TOP=../..
include $(TOP)/configure/CONFIG
#----------------------------------------
#  ADD MACRO DEFINITIONS AFTER THIS LINE
#=============================

# The following gets rid of the -fno-implicit-templates flag on vxWorks, 
# so we get automatic template instantiation.
# This is what we want for the source files that define template functions.
#ifeq (vxWorks,$(findstring vxWorks, $(T_A)))
#CODE_CXXFLAGS=
#endif

INC += NDPluginDimFei.h dimfei.h dist.h linsys.h stdafx.h utilities.h targetver.h

LIBRARY_IOC += NDPluginDimFei

NDPluginDimFei_SRCS += NDPluginDimFei.cpp dimfei.cpp dist.cpp linsys.cpp stdafx.cpp

USR_LDFLAGS += -lm -lblas -llapack -llapacke

DBD += NDPluginDimFei.dbd
#DBD += base.dbd
#DBD += asyn.dbd
#DBD += ADSupport.dbd
#DBD += NDPluginSupport.dbd

#LIBS += NDPlugin
#LIBS += ADBase
#LIBS += asyn

include $(ADCORE)/ADApp/commonLibraryMakefile

include $(TOP)/configure/RULES
#----------------------------------------
#  ADD RULES AFTER THIS LINE

