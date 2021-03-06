HOW TO INSTALL CODEQUERY IN LINUX
=================================

This INSTALL guide applies to Linux only

(For Windows, a SETUP EXE package will be provided)


## HOW TO INSTALL IN LINUX?

1. Install CMake (>2.7), sqlite3, Qt4 (>4.7), QScintilla (2.6 or higher), cscope (15.8a or higher), ctags. If you have Ubuntu, Linux Mint, Debian or Fedora installed, most of these should be obtainable through the package managers. Note that the cscope version on the Ubuntu repositories may not be the latest one. It's better to have the latest version of cscope installed.   
[CMake](http://www.cmake.org/)   
[sqlite3](http://www.sqlite.org/)   
[Qt4](http://qt-project.org/)   
[cscope](http://cscope.sourceforge.net/)   
[ctags](http://ctags.sourceforge.net/)    
[pycscope](https://github.com/portante/pycscope)    
[QScintilla](http://www.riverbankcomputing.com/software/qscintilla/intro)    

In Ubuntu, do the following:    
```bash
sudo apt-get install g++ git cmake sqlite3 libsqlite3-dev qt4-dev-tools libqscintilla2-dev cscope exuberant-ctags rpm
```
In Fedora, do the following:    
```bash
sudo yum install gcc-c++ git cmake sqlite sqlite-devel qt-devel qscintilla-devel cscope ctags rpm-build
```

2. Download the repository as a ZIP file from github or clone git repository:
[codequery@github](https://github.com/ruben2020/codequery)
```bash
git clone https://github.com/ruben2020/codequery.git
```

3. Unzip to a directory and change to that directory.
```bash
cd ~/workspace/codequery
```

4. Create a directory called build and change to it.
```bash
mkdir build
cd build
```

5. Run cmake, make and make install.
```bash
cmake -G "Unix Makefiles" ..
make
sudo make install
```
If you want to install to an alternative directory instead of the default one, use the following:
```bash
cmake -DCMAKE_INSTALL_PREFIX="/home/johndoe/tools/" -G "Unix Makefiles" ..
make
make install
```

6. Please read [HOWTO-LINUX](HOWTO-LINUX.md) to learn how to use this software.

