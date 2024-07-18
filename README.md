# Qt6 auto deploy demo
eton@240718

usage:
```sh
mkdir build && cd build 
cmake ..
cmake --build . -j
mkdir /tmp/install34 && cmake --install .  --prefix /tmp/install34
tree /tmp/install34
```
you will see the all app and dependences, it is very good.

Ref:
- [Qt6 Manual:Qt 6.5/Qt Core/CMake Commands in Qt6 Core/qt_generate_deploy_app_script/Qt 6.5.3 Reference Documentation]()
