cmake_minimum_required(VERSION 3.16)

project(qt6-cmake-deploy-01 VERSION 0.1 LANGUAGES CXX)

set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(Qt6 6.5 REQUIRED COMPONENTS Quick Core)

qt_standard_project_setup(REQUIRES 6.5)
set(MyApp "appqt6-cmake-deploy-01")
qt_add_executable(${MyApp}
    main.cpp
)

qt_add_qml_module(${MyApp}
    URI qt6-cmake-deploy-01
    VERSION 1.0
    QML_FILES Main.qml
)

# Qt for iOS sets MACOSX_BUNDLE_GUI_IDENTIFIER automatically since Qt 6.1.
# If you are developing for iOS or macOS you should consider setting an
# explicit, fixed bundle identifier manually though.
set_target_properties(${MyApp} PROPERTIES
#    MACOSX_BUNDLE_GUI_IDENTIFIER com.example.${MyApp}
    MACOSX_BUNDLE_BUNDLE_VERSION ${PROJECT_VERSION}
    MACOSX_BUNDLE_SHORT_VERSION_STRING ${PROJECT_VERSION_MAJOR}.${PROJECT_VERSION_MINOR}
    MACOSX_BUNDLE TRUE
    WIN32_EXECUTABLE TRUE
)

target_link_libraries(${MyApp}
    PRIVATE Qt6::Quick
)

include(GNUInstallDirs)
install(TARGETS ${MyApp}
    BUNDLE DESTINATION .
    LIBRARY DESTINATION ${CMAKE_INSTALL_LIBDIR}
    RUNTIME DESTINATION ${CMAKE_INSTALL_BINDIR}
)
qt_generate_deploy_app_script(
     TARGET ${MyApp}
     OUTPUT_SCRIPT deploy_script
     NO_UNSUPPORTED_PLATFORM_ERROR)

install(SCRIPT ${deploy_script})
