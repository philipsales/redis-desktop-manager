# Redis Desktop Manager - v.0.9.4 
| Operating System | Testing |
| ------ | ------ |
| Sierra 10.12 | Yes |
## Getting Started
### Prerequisites
1. Homebrew
1. XCode
1. Qt Creator
### Build from source for MacOS X
1. Get the source code
    ```bash
    git clone --recursive https://github.com/uglide/RedisDesktopManager.git -b 0.9 rdm 
    cd ./rdm
    ```
1. Install [XCode](https://developer.apple.com/xcode/) with Xcode build tools

1. Install [Homebrew](http://brew.sh/)

1. Create a copy of Info.plist from sample
    ```bash
    cd ./src && cp ./resources/Info.plist.sample ./resources/Info.plist
    ```
1. Building RDM dependencies require i.a. openssl and cmake. Install them:
    ```bash 
    brew install openssl cmake
    ```
1. Build RDM dependencies
    ```bash
    ./configure
    ```
1. Install whole Qt package [Qt 3.0.5](http://ftp.jaist.ac.jp/pub/qtproject/archive/online_installers/3.0/qt-unified-mac-x64-3.0.5-online.dmg) 
1. Open project ./src/rdm.pro in Qt Creator
1. Change the `CONFIG-=app_bundle` to `CONFIG+=app_bundle` in `line 76` 
1. Run it for the first time to create `rdm.app`
1. Copy the folder rdm/3rdparty/crashreporter to rdm/bin/osx/debug/
     ```bash
    cp -Rf $DIRPATH/rdm/3rdparty/crashreporter $DIRPATH/rdm/bin/osx/debug/
    ```
1. Run the `macdeployqt`
    ```bash
     /Users/<username>/Qt/5.11.1/clang_64/bin/macdeployqt rdm.app -dmg -qmldir=/Users/<username>/$DIRPATH/rdm/src/qml
    ```
1. Run build again to generate the `rdm.dmg` in the $PATH/rdm/bin/osx/debug/
1. Transfer the `rdm.dmg` to MacOS `Applications` folder
## Running the tests
## Deployment
## Built With
## Contributing
## Versioning
[Redis Desktop Manger 0.9.4](https://github.com/uglide/RedisDesktopManager/releases)
## Authors
* **Philip Sales** - *adopted work*
## License
This project is licensed under the MIT - see the Types of [Licenses](https://opensource.org/licenses/alphabetical) 
## Acknowledgments
* [Redis Desktop Manger](https://redisdesktop.com/)


