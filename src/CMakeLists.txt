include_directories(${CMAKE_CURRENT_SOURCE_DIR})

add_subdirectory(app)
add_subdirectory(base)

if (WIN32)
    target_link_libraries(qbt_app PRIVATE powrprof)
endif()

if (GUI)
    add_subdirectory(gui)
endif()

if (WEBUI)
    add_subdirectory(webui)
endif()
