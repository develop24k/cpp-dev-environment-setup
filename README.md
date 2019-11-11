### How to Setup C++ Dev Environment on Windows 10

##### High Level Steps
1) Download and Install **Eclipse IDE for C/C++ Developers**
2) Download and Install **MinGW** GNU Compiler Collection (GCC)
3) Setup compiler path in **Eclipse IDE** pointing to **MinGW**

------------

####Details
- Goto google.com and search for **Eclipse IDE for C/C++ Developers**
- Downlaod the latest x64 bit version ZIP file for the IDE.
- Extract it on C:\
- Ensure C:\eclipse\eclipse.exe exists.
- Goto https://osdn.net/projects/mingw/
- Download mingw-get-setup.exe
- Run mingw-get-setup.exe to Install **MinGW Installation Manager**
	- Select the default installation path for MinGW i.e. C:\MinGW
	- During the installation it will prompt you to select required packages.
	- Select **mingw32-base-bin** and **mingw32-gcc-g++-bin**
	- Proceed further and finish the Installation.
	- Ensure you have **C:\MinGW\lib\gcc\mingw32** path now.
- Create System Environemnt Variables -
	-  MINGW_HOME = **C:\MinGW**
	- Append Path with **%MINGW_HOME%\bin** 
- Run C:\eclipse\eclipse.exe as admin to launch **Eclipse IDE**
- Setup workspace
- Go to File Menu and create a new **C++ Project**.
- While on the **Project Explorer** open on the left side, go to the **Project** menu and select **Properties**.
- Go to **C/C++ General** -> **Paths and Symbols**.
- Under the **Includes** tab Add the following settings for **GNU C** and **GNU C++**
	- GNU C
		- ${MINGW_HOME}\include
		- ${MINGW_HOME}\lib\gcc\mingw32\8.2.0\include
		- ${MINGW_HOME}\lib\gcc\mingw32\8.2.0\include-fixed
	- GNU C++
		- ${MINGW_HOME}\include
		- ${MINGW_HOME}\lib\gcc\mingw32\8.2.0\include\c++
		- ${MINGW_HOME}\lib\gcc\mingw32\8.2.0\include\c++\mingw32
		- ${MINGW_HOME}\lib\gcc\mingw32\8.2.0\include\c++\backward
		- ${MINGW_HOME}\lib\gcc\mingw32\8.2.0\include
		- ${MINGW_HOME}\lib\gcc\mingw32\8.2.0\include-fixed
- Note: Update the above path based on mingw version you downloaded.
- Write a C++ program and Run/Debug it as C++ Local Application


------------
develop24k@gmail.com
