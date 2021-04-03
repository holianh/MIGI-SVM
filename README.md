# MIGI-SVM
Cài đặt môi trường cho MiGi VSM project

# Các yêu cầu ràng buộc:

1. Cài Win10x64
2. Cài [VS2015](https://kynguyencongnghe.com/key-ban-quyen-visual-studio-2015-vinh-vien/) (dùng compiler C++)
3. Cài Mapble mới nhất (ver hiện tại: Marble-setup_2.2.0-1_x64): [Marble 2.2.0 (Windows 64-bit)](https://marble.kde.org/install.php?)

[link cài](https://community.kde.org/Marble/WindowsCompiling#Compiling_Marble_using_Microsoft_Visual_C.2B.2B_and_Visual_Studio)

Chúng ta sẽ cài Mable từ src code: [Source code](https://invent.kde.org/education/marble):

Cài phần premilier:

1. Cài Git repository: http://git-scm.com/downloads, cài OK: chạy git trong CMD ok là dc
2. Cài Cmake: http://www.cmake.org/, chạy cmake trong CMD dc là dc
3. Cài Qt community edition for Windows:https://www.qt.io/download/
4. cài theo: "Compiling Marble using Microsoft Visual C++ and nmake":
thêm  `C:\Qt\Qt5.6.2\5.6\msvc2015\bin` vào system path.
5.  



git vào thư mục ./marble/sources
```
git clone https://invent.kde.org/education/marble.git ./marble/sources

mkdir -p marble/build
cd ./marble/build
cmake -DCMAKE_BUILD_TYPE=Debug -DWITH_KF5=TRUE -DCMAKE_INSTALL_PREFIX=c:\mable  ..\sources
make
sudo make install


```

5. Cài [Vcpkg](https://github.com/Microsoft/vcpkg#quick-start-windows)
    ```
    git clone https://github.com/microsoft/vcpkg
     .\vcpkg\bootstrap-vcpkg.bat
     .\vcpkg\vcpkg integrate install
    ```
5. Cài [protobuf](https://github.com/protocolbuffers/protobuf/blob/master/src/README.md#c-installation---windows): Cài bản mới nhất, phiên bản đã dùng [protoc-3.15.7-win64](https://github.com/protocolbuffers/protobuf/releases/download/v3.15.7/protoc-3.15.7-win64.zip)

Bản mới nhất sẽ được cài khi chạy lệnh: `.\vcpkg\vcpkg install protobuf protobuf:x64-windows`

7. 
