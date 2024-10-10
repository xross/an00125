cmake_minimum_required(VERSION 3.21)
include($ENV{XMOS_CMAKE_PATH}/xcommon.cmake)
project(app_mass_storage)

set(APP_HW_TARGET XK-EVK-XU316)

set(APP_INCLUDES src)

set(APP_COMPILER_FLAGS -O3 -report -DUSE_XSCOPE=1 -fxscope -lflash)

set (APP_DEPENDENT_MODULES "lib_xud(2.3.2)"
                          "lib_logging(3.2.0)"
                          "lib_xassert(4.2.0)"
                          )

set(XMOS_SANDBOX_DIR ${CMAKE_CURRENT_LIST_DIR}/../..)

XMOS_REGISTER_APP()
