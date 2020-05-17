# qt_pocmon 
Linux build  
[![Build Status](https://travis-ci.com/kwl3434/qt_procmon.svg?branch=master)](https://travis-ci.com/kwl3434/qt_procmon)<br>
Windows build <br>
[![Build status](https://ci.appveyor.com/api/projects/status/h7g4lej3tbm3fhb0?svg=true)](https://ci.appveyor.com/project/kwl3434/qt-procmon)
### build step
1. clone project <br>
2. windows : https://github.com/kwl3434/qt_procmon/wiki/QT-Windows-environment <br>
   linux : https://github.com/kwl3434/qt_procmon/wiki/QT-Linux(Ubuntu)-environment <br>
3. https://github.com/kwl3434/qt_procmon/wiki/Cmake-Config(Windows-Linux) <br>
4. https://github.com/kwl3434/qt_procmon/wiki/gtest-config(Windows-Linux) <br>
5. windows run qt_procmon.sln build all <br>
   Linux run qt_procmon/Src/build_all_Release.sh <br>
```
qt_procmon/
├── build
│   ├── Linux
│   │    ├── x64_x86
│   │    │   ├── Release
│   │    │   └── Debug
│   │    └── i386
│   │        ├── Release
│   │        └── Debug
│   └── Win
│        ├── x64
│        │   ├── Release
│        │   └── Debug
│        └── x32
│            ├── Release
│            └── Debug
├── CODE_OF_CONDUCT.md
├── CONTRIBUTING.md
├── images
│   ├── qt install images
│   │   └── *.PNG
│   ├── ubuntu qt images
│   │   └── *.PNG
│   └── Windows cmake images
│       └── *.PNG
├── LICENSE
├── README.md
└── Src
    ├── build_all_Debug.sh
    ├── build_all_Release.sh
    ├── CMakeLists.txt
    ├── CMakeSettings.json
    ├── helloworld
    │   └── qt-main.cpp
    └── Makefile

```
