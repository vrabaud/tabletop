if (ROS_GROOVY_FOUND)
configure_file(${CMAKE_CURRENT_SOURCE_DIR}/__init__.py.plain.in
               ${CATKIN_DEVEL_PREFIX}/${CATKIN_PACKAGE_PYTHON_DESTINATION}/ecto_cells/__init__.py
               @ONLY
)

install(FILES ${CATKIN_DEVEL_PREFIX}/${CATKIN_PACKAGE_PYTHON_DESTINATION}/ecto_cells/__init__.py
        DESTINATION ${CATKIN_PACKAGE_PYTHON_DESTINATION}/ecto_cells/__init__.py
)
else()
configure_file(__init__.py.plain.in
               ${CATKIN_DEVEL_PREFIX}/${CATKIN_PACKAGE_PYTHON_BUILD_DESTINATION}/ecto_cells/__init__.py
               @ONLY
)

install(FILES ${CATKIN_DEVEL_PREFIX}/${CATKIN_PACKAGE_PYTHON_BUILD_DESTINATION}/ecto_cells/__init__.py
        DESTINATION ${CATKIN_PACKAGE_PYTHON_DESTINATION}/ecto_cells/__init__.py
)
endif()
