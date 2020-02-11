# waddacat
git clone --recursive https://github.com/yuzu-emu/yuzu
cd yuzu
git submodule update --init --recursive
git clone --recursive https://github.com/yuzu-emu/yuzu-mainline
cd yuzu-mainline
git submodule update --init --recursive
export Qt5_DIR=$(brew --prefix)/opt/qt5
export MACOSX_DEPLOYMENT_TARGET=10.14
mkdir build
cd build
cmake .. -DCMAKE_BUILD_TYPE=Release
make -j4
