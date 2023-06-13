cmake_minimum_required(VERSION 3.16)

project(game LANGUAGES CXX)

find_package(Qt6 REQUIRED COMPONENTS Core Gui Widgets)

qt_standard_project_setup()

qt_add_executable(game main.cpp Game.cpp)

find_package(QString REQUIRED)
find_package(QGraphicsItem REQUIRED)
SET(QT_USE_QTDESIGNER ON)

set_target_properties(game PROPERTIES
    WIN32_EXECUTABLE TRUE
    MACOSX_BUNDLE TRUE
)

target_link_libraries(game PRIVATE
    Qt6::Core
    Qt6::Gui
    Qt6::Widgets
)