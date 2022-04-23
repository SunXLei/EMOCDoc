---
weight: 1
bookFlatSection: false
title: "Install"
---

# Installing EMOC
EMOC is now available on Windows, Linux and MacOS. There are few steps need to install EMOC as below.

## Dependency

1. [**CMake**](https://cmake.org/)

   CMake is an open-source, cross-platform family of tools designed to build, test and package software. EMOC uses it to generate the build system files on different platforms. You can download it from [here](https://cmake.org/download/). The minimum needed version of CMake is 3.10. For more information please refer to the [CMake documentation](https://cmake.org/documentation/).

2. [**Visual Studio 2019**](https://visualstudio.microsoft.com/) (for windows)

   Visual Studio (VS) is an Integrated Development Environment (IDE) for C++. EMOC generates the VS project file on Windows to compile the source code. You can download it from [here](https://visualstudio.microsoft.com/downloads) .

3. [**Gnuplot**](http://www.gnuplot.info/) (for windows)

   Gnuplot is a portable command-line driven graphing utility. EMOC uses it to provide some visualization functions. The installation for Linux and MacOS is handled in the build script files. For windows, users need to install it from [here](https://sourceforge.net/projects/gnuplot/files/gnuplot/5.0.1/). We recommend to use the version 5.0.1. 

4. [**Git**](https://git-scm.com/) (optional)

   You can use git to download the EMOC source code from github conveniently or just click the download button on the EMOC github page directly.

## Get the Source Code

### **Use git command**

If you have git installed on your system, use `git clone` command to get the EMOC source code as below:

```bash
git clone https://github.com/SunXLei/EMOC.git
```

### **Download from github page**

Go to the [EMOC github page](https://github.com/SunXLei/EMOC) and click the option 'Download ZIP':

![image](../../images/github_download.png)

and unzip the file wherever you want.



## Build

When you have got the source code, go to the root directory of EMOC. We have prepared some script files for the ease of building EMOC.

### **For Windows**

Double-click the file 'build_window.bat', it will detect the Visual Studio installed on your system and generate the project file automatically. After executing the '.bat' file, go to the **'/build'** directory and open the 'EMOC.sln' file with Visual Studio.

You can travel the code and run it in VS directly or find the executable file **'EMOC.exe'** in root directory after compiling it.

### **For Linux and MacOS**

Open the terminal and change the current directory to the root directory of EMOC. Build EMOC with following command:

**Linux:**

```bash
bash ./build_linux.sh
```

**MacOS:**

```bash
bash ./build_macos.sh
```

The executable file **'EMOC'** will appear in the root directory when building successfully.