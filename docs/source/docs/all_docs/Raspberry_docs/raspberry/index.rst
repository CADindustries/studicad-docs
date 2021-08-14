Raspberry pi setup
======================================

Here is some info about how to setup raspberry pi.

PWM setup:
^^^^^^^^^^^^^^^^^^^^^^^

Go to `this <https://github.com/sarfata/pi-blaster>`__  repo and install it using **Build and install directly from source**

OpenCV setup:
^^^^^^^^^^^^^^^^^^^^^^^

1. Open up bash on your raspberry  
  
2. Type this commands there:  
  
.. code-block:: bash
	:linenos:

	sudo apt update
	sudo apt upgrade
	sudo apt-get update
	sudo apt-get upgrade

	sudo dpkg --add-architecture armhf
	sudo apt update
	sudo apt install qemu-user-static

	sudo apt install libgtk-3-dev:armhf libcanberra-gtk3-dev:armhf

	sudo apt install libtiff-dev:armhf zlib1g-dev:armhf
	sudo apt install libjpeg-dev:armhf libpng-dev:armhf
	sudo apt install libavcodec-dev:armhf libavformat-dev:armhf libswscale-dev:armhf libv4l-dev:armhf
	sudo apt-get install libxvidcore-dev:armhf libx264-dev:armhf

	sudo apt install crossbuild-essential-armhf
	sudo apt install gfortran-arm-linux-gnueabihf

	sudo apt install cmake git pkg-config wget

3. On ``sudo apt install gfortran-arm-linux-gnueabihf`` could be a **error**. Sultion could be on the site https://www.raspberrypi.org/forums/viewtopic.php?t=235145.  

.. code-block:: bash
	:linenos:

	// So according to this howto what you did is:	

	$ sudo su
	# apt-cache madison hostapd
   	 hostapd | 2:2.6-21~bpo9~rpt1 | http://archive.raspberrypi.org/debian stretch/main armhf Packages
   	 hostapd | 2:2.4-1+deb9u2 | http://raspbian.raspberrypi.org/raspbian stretch/main armhf Packages
	# apt-get install hostapd=2:2.4-1+deb9u2 -V

	// I fogot, you would like to prevent future update with:

	# apt-mark hold hostapd

	// And remove the directive later with:
	
	# apt-mark unhold hostapd

	// IF THERE IS STILL THE ERROR TRY UPPER AFTER BELOW

	// The fix for me is to edit /etc/default/hostapd and set DAEMON_CONF="/etc/hostapd/hostapd.conf"

	// hostapd FILE COULD NOT BE THERE SO CREATE IT THEN

	// I found the problem by adding:

	logger_syslog=-1

	// to the

	/etc/hostapd/hostapd.conf

	// file. Then running

	sudo cat /var/log/syslog | grep hostapd 

	// to see the error messages.

	// THIS SHOULD HELP

4. Then:  
  
.. code-block:: bash
	:linenos:

	cd ~
	mkdir opencv_all && cd opencv_all
	wget -O opencv.tar.gz https://github.com/opencv/opencv/archive/4.4.0.tar.gz
	tar xf opencv.tar.gz
	wget -O opencv_contrib.tar.gz https://github.com/opencv/opencv_contrib/archive/4.4.0.tar.gz
	tar xf opencv_contrib.tar.gz

	export PKG_CONFIG_PATH=/usr/lib/arm-linux-gnueabihf/pkgconfig:/usr/share/pkgconfig
	export PKG_CONFIG_LIBDIR=/usr/lib/arm-linux-gnueabihf/pkgconfig:/usr/share/pkgconfig

	cd opencv-4.4.0
	mkdir build && cd build

5. Then cmake:

.. code-block:: bash
	:linenos:

	cmake -D CMAKE_BUILD_TYPE=RELEASE \
	-D CMAKE_INSTALL_PREFIX=/opt/opencv-4.4.0 \
	-D CMAKE_TOOLCHAIN_FILE=../platforms/linux/arm-gnueabi.toolchain.cmake \
	-D OPENCV_EXTRA_MODULES_PATH=~/opencv_all/opencv_contrib-4.4.0/modules \
	-D OPENCV_ENABLE_NONFREE=ON \
	-D ENABLE_NEON=ON \
	-D ENABLE_VFPV3=ON \
	-D BUILD_TESTS=OFF \
	-D BUILD_DOCS=OFF \
	-D BUILD_EXAMPLES=OFF ..

.. code-block:: bash
	:linenos:

	make -j16

.. code-block:: bash
	:linenos:

	sudo make install/strip

6. Here also could be a error while creating Makefile. Solution here: https://github.com/abhiTronix/raspberry-pi-cross-compilers/issues/60. 
Source site: https://habr.com/ru/post/461693/ and https://solarianprogrammer.com/2018/12/18/cross-compile-opencv-raspberry-pi-raspbian/.

7. Into bash: ``nano ~/.bashrc`` and add lines:

.. code-block:: bash
	:linenos:
	
	export ANT_HOME=/usr/share/ant/
	export PATH=${PATH}:${ANT_HOME}/bin
	export JAVA_HOME=/usr/lib/jvm/java-11-openjdk-armhf/
	export PATH=$PATH:$JAVA_HOME/bin

8. Reboot raspberry

9. Then:

.. code-block:: bash
	:linenos:

	cd ~
	mkdir opencv_r && cd opencv_r
	wget https://codeload.github.com/Itseez/opencv/zip/4.4.0
	mv 4.4.0 opencv.zip
	unzip opencv.zip 
	cd opencv-4.4.0/
	mkdir build && cd build

10. Then cmake:

.. code-block:: bash
	:linenos:

	cmake -D CMAKE_BUILD_TYPE=RELEASE \
	-D OPENCV_EXTRA_MODULES_PATH=/home/pi/opencv_all/opencv_contrib-4.4.0/modules \
	-D JAVA_INCLUDE_PATH=$JAVA_HOME/include \
	-D CMAKE_TOOLCHAIN_FILE=../platforms/linux/arm-gnueabi.toolchain.cmake \
	-D JAVA_AWT_LIBRARY=$JAVA_HOME/jre/lib/amd64/libawt.so \
	-D JAVA_JVM_LIBRARY=$JAVA_HOME/jre/lib/arm/server/libjvm.so \
	-D CMAKE_INSTALL_PREFIX=/usr/local ..

.. code-block:: bash
	:linenos:

	make
	sudo make install

Source: https://robinhenniges.com/part-1-installing-opencv-3-1-0-on-raspberry-pi-debian-jessy-with-java-library/.

11. Also you should check if you camera works using ``raspistill -o Desktop/image.jpg``. 
If there is a error like *you should update firmware and smth like that* then your camera is broken. 
My question on stackexchange: https://raspberrypi.stackexchange.com/questions/127622/build-opencv-for-java-on-rpi4/