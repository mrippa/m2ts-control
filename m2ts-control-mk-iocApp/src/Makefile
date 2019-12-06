TOP=../..

include $(TOP)/configure/CONFIG
#----------------------------------------
#  ADD MACRO DEFINITIONS AFTER THIS LINE
#=============================

#=============================
# Build the IOC application

PROD_IOC = m2ts-control-mk-ioc
# m2ts-control-mk-ioc.dbd will be created and installed
DBD += m2ts-control-mk-ioc.dbd

# m2ts-control-mk-ioc.dbd will be made up from these files:
m2ts-control-mk-ioc_DBD += base.dbd

# Include dbd files from all support modules:
#m2ts-control-mk-ioc_DBD += xxx.dbd

# Add all the support libraries used by this IOC
# m2ts-control-mk-ioc_LIBS += xxx
# m2ts-control-mk-ioc_LIBS += seq pv seqDev

# m2ts-control-mk-ioc_registerRecordDeviceDriver.cpp derives from m2ts-control-mk-ioc.dbd
m2ts-control-mk-ioc_SRCS += m2ts-control-mk-ioc_registerRecordDeviceDriver.cpp

# Build the main IOC entry point on workstation OSs.
m2ts-control-mk-ioc_SRCS_DEFAULT += m2ts-control-mk-iocMain.cpp

# Finally link to the EPICS Base libraries
m2ts-control-mk-ioc_LIBS += $(EPICS_BASE_IOC_LIBS)

#===========================

include $(TOP)/configure/RULES
#----------------------------------------
#  ADD RULES AFTER THIS LINE

