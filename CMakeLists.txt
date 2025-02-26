cmake_minimum_required(VERSION 3.22)
project(open3d)

# https://github.com/isl-org/Open3D/releases
set(O3D_VERSION   0.19.0)
set(O3D_URL_MD5   752d07c5cad260495fd97dedf9aa5141)

set(O3D_URL       https://github.com/isl-org/Open3D/releases/download/v${O3D_VERSION}/open3d-devel-linux-x86_64-cxx11-abi-${O3D_VERSION}.tar.xz)

include(ExternalProject)
ExternalProject_Add(o3d_archive
  URL               ${O3D_URL}
  URL_MD5           ${O3D_URL_MD5}
  DOWNLOAD_EXTRACT_TIMESTAMP  true
  PREFIX            o3d_archive
  CONFIGURE_COMMAND ""
  BUILD_COMMAND     ""
  INSTALL_COMMAND   ""
)

ExternalProject_Get_Property(o3d_archive SOURCE_DIR)
set(O3D_PATH ${SOURCE_DIR})

install(DIRECTORY ${O3D_PATH}/
    DESTINATION .
)
