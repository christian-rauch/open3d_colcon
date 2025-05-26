cmake_minimum_required(VERSION 3.22)
project(open3d)

set(open3d_colcon_MAJOR_VERSION 0)
set(open3d_colcon_MINOR_VERSION 0)
set(open3d_colcon_PATCH_VERSION 0)
set(open3d_colcon_VERSION
  ${open3d_colcon_MAJOR_VERSION}.${open3d_colcon_MINOR_VERSION}.${open3d_colcon_PATCH_VERSION})

if(CMAKE_COMPILER_IS_GNUCXX OR CMAKE_CXX_COMPILER_ID MATCHES "Clang")
  add_compile_options(-Wall -Wextra -Wpedantic)
endif()

# uncomment the following section in order to fill in
# further dependencies manually.
# find_package(<dependency> REQUIRED)
