CMAKE_MINIMUM_REQUIRED(VERSION 2.8.9)

PROJECT(VIBes_viewer)
SET(CMAKE_AUTOMOC ON)
SET(CMAKE_INCLUDE_CURRENT_DIR ON)

FIND_PACKAGE(Qt5Core REQUIRED)
FIND_PACKAGE(Qt5Widgets REQUIRED)
FIND_PACKAGE(Qt5Gui REQUIRED)

SET(VIBes_viewer_SOURCES main.cpp figure2d.cpp vibestreemodel.cpp vibeswindow.cpp)
SET(VIBes_viewer_FORMS vibeswindow.ui)

QT5_WRAP_UI(VIBes_viewer_FORMS_HEADERS ${VIBes_viewer_FORMS})

ADD_EXECUTABLE(VIBes-viewer ${VIBes_viewer_SOURCES} ${VIBes_viewer_FORMS_HEADERS})
QT5_USE_MODULES(VIBes-viewer Widgets Gui Core Svg)