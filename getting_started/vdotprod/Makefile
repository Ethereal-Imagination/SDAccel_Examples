# vdotprod Application

include ../../utility/boards.mk
include ../../libs/xcl_cpp/xcl_cpp.mk
include ../../libs/opencl/opencl.mk

# vdotprod Host Application
vdotprod_SRCS=./src/vdotprod.cpp $(xcl_cpp_SRCS)
vdotprod_HDRS=./src/vdotprod.h $(xcl_cpp_HDRS)
vdotprod_EXE=vdotprod
vdotprod_CXXFLAGS=-I./src/ $(opencl_CXXFLAGS) $(xcl_cpp_CXXFLAGS)
vdotprod_X86_LDFLAGS=$(opencl_X86_LDFLAGS)
vdotprod_POWER_LDFLAGS=$(opencl_POWER_LDFLAGS)

# hello Kernel
krnl_vdotprod_SRCS=./src/krnl_vdotprod.cl

EXES=vdotprod
XCLBINS=krnl_vdotprod

include ../../utility/rules.mk

