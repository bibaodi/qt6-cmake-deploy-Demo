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
## Appendix-my list: 
`tree /tmp/install34` output is in below:
```
/tmp/install34/
├── bin
│   ├── appqt6-cmake-deploy-01
│   └── qt.conf
├── lib
│   ├── libicudata.so.56 -> libicudata.so.56.1
│   ├── libicudata.so.56.1
│   ├── libicui18n.so.56 -> libicui18n.so.56.1
│   ├── libicui18n.so.56.1
│   ├── libicuuc.so.56 -> libicuuc.so.56.1
│   ├── libicuuc.so.56.1
│   ├── libQt6Core.so.6 -> libQt6Core.so.6.5.3
│   ├── libQt6Core.so.6.5.3
│   ├── libQt6DBus.so.6 -> libQt6DBus.so.6.5.3
│   ├── libQt6DBus.so.6.5.3
│   ├── libQt6EglFSDeviceIntegration.so.6 -> libQt6EglFSDeviceIntegration.so.6.5.3
│   ├── libQt6EglFSDeviceIntegration.so.6.5.3
│   ├── libQt6EglFsKmsSupport.so.6 -> libQt6EglFsKmsSupport.so.6.5.3
│   ├── libQt6EglFsKmsSupport.so.6.5.3
│   ├── libQt6Gui.so.6 -> libQt6Gui.so.6.5.3
│   ├── libQt6Gui.so.6.5.3
│   ├── libQt6Network.so.6 -> libQt6Network.so.6.5.3
│   ├── libQt6Network.so.6.5.3
│   ├── libQt6OpenGL.so.6 -> libQt6OpenGL.so.6.5.3
│   ├── libQt6OpenGL.so.6.5.3
│   ├── libQt6Pdf.so.6 -> libQt6Pdf.so.6.5.3
│   ├── libQt6Pdf.so.6.5.3
│   ├── libQt6QmlModels.so.6 -> libQt6QmlModels.so.6.5.3
│   ├── libQt6QmlModels.so.6.5.3
│   ├── libQt6Qml.so.6 -> libQt6Qml.so.6.5.3
│   ├── libQt6Qml.so.6.5.3
│   ├── libQt6Quick3DUtils.so.6 -> libQt6Quick3DUtils.so.6.5.3
│   ├── libQt6Quick3DUtils.so.6.5.3
│   ├── libQt6Quick.so.6 -> libQt6Quick.so.6.5.3
│   ├── libQt6Quick.so.6.5.3
│   ├── libQt6Svg.so.6 -> libQt6Svg.so.6.5.3
│   ├── libQt6Svg.so.6.5.3
│   ├── libQt6XcbQpa.so.6 -> libQt6XcbQpa.so.6.5.3
│   └── libQt6XcbQpa.so.6.5.3
├── plugins
│   ├── egldeviceintegrations
│   │   ├── libqeglfs-emu-integration.so
│   │   ├── libqeglfs-kms-egldevice-integration.so
│   │   └── libqeglfs-x11-integration.so
│   ├── iconengines
│   │   └── libqsvgicon.so
│   ├── imageformats
│   │   ├── libqgif.so
│   │   ├── libqicns.so
│   │   ├── libqico.so
│   │   ├── libqjpeg.so
│   │   ├── libqpdf.so
│   │   ├── libqsvg.so
│   │   ├── libqtga.so
│   │   ├── libqtiff.so
│   │   ├── libqwbmp.so
│   │   └── libqwebp.so
│   ├── networkinformation
│   │   ├── libqglib.so
│   │   └── libqnetworkmanager.so
│   ├── platforms
│   │   └── libqxcb.so
│   ├── qmltooling
│   │   ├── libqmldbg_debugger.so
│   │   ├── libqmldbg_inspector.so
│   │   ├── libqmldbg_local.so
│   │   ├── libqmldbg_messages.so
│   │   ├── libqmldbg_nativedebugger.so
│   │   ├── libqmldbg_native.so
│   │   ├── libqmldbg_preview.so
│   │   ├── libqmldbg_profiler.so
│   │   ├── libqmldbg_quick3dprofiler.so
│   │   ├── libqmldbg_quickprofiler.so
│   │   ├── libqmldbg_server.so
│   │   └── libqmldbg_tcp.so
│   ├── tls
│   │   └── libqopensslbackend.so
│   └── xcbglintegrations
│       ├── libqxcb-egl-integration.so
│       └── libqxcb-glx-integration.so
└── translations
    ├── qt_ar.qm
    ├── qt_bg.qm
    ├── qt_ca.qm
    ├── qt_cs.qm
    ├── qt_da.qm
    ├── qt_de.qm
    ├── qt_en.qm
    ├── qt_es.qm
    ├── qt_fa.qm
    ├── qt_fi.qm
    ├── qt_fr.qm
    ├── qt_gd.qm
    ├── qt_gl.qm
    ├── qt_he.qm
    ├── qt_hr.qm
    ├── qt_hu.qm
    ├── qt_it.qm
    ├── qt_ja.qm
    ├── qt_ko.qm
    ├── qt_lt.qm
    ├── qt_lv.qm
    ├── qt_nl.qm
    ├── qt_nn.qm
    ├── qt_pl.qm
    ├── qt_pt_BR.qm
    ├── qt_pt_PT.qm
    ├── qt_ru.qm
    ├── qt_sk.qm
    ├── qt_sl.qm
    ├── qt_sv.qm
    ├── qt_tr.qm
    ├── qt_uk.qm
    ├── qt_zh_CN.qm
    └── qt_zh_TW.qm

13 directories, 102 files
```
