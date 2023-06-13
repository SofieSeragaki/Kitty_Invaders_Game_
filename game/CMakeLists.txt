cmake_minimum_required(VERSION 3.24.2)
project(Kitty_Invaders_Game_)

set(CMAKE_CXX_STANDARD 14)

find_package(Qt6 REQUIRED COMPONENTS Core Gui Widgets)

qt_standard_project_setup()

qt_add_executable(Kitty_Invaders_Game_
        Bullet.cpp
        Bullet.h
        Button.cpp
        Button.h
        Enemy.cpp
        Enemy.h
        Game.cpp
        Game.h
        Health.cpp
        Health.h
        main.cpp
        Player.cpp
        Player.h
        Score.cpp
        Score.h)

set_target_properties(Kitty_Invaders_Game_ PROPERTIES
        WIN32_EXECUTABLE TRUE
        MACOSX_BUNDLE TRUE
        )

target_link_libraries(Kitty_Invaders_Game_ PRIVATE
        Qt6::Core
        Qt6::Gui
        Qt6::Widgets
        
        )