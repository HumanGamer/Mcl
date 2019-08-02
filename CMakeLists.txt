cmake_minimum_required(VERSION 2.8)

project(Mcl)

include_directories(include)

set (Main_SRC
    # Sources
    src/CMclAutoLock.cpp
    src/CMclAutoPtr.cpp
    src/CMclCritSec.cpp
    src/CMclEvent.cpp
    src/CMclGlobal.cpp
    src/CMclKernel.cpp
    src/CMclMailbox.cpp
    src/CMclMonitor.cpp
    src/CMclMutex.cpp
    src/CMclSemaphore.cpp
    src/CMclSharedMemory.cpp
    src/CMclThread.cpp
    src/CMclWaitableCollection.cpp
    
    # Headers
    include/CMcl.h
    include/CMclAutoLock.h
    include/CMclAutoPtr.h
    include/CMclCritSec.h
    include/CMclEvent.h
    include/CMclGlobal.h
    include/CMclKernel.h
    include/CMclLinkedLists.h
    include/CMclMailbox.h
    include/CMclMonitor.h
    include/CMclMutex.h
    include/CMclSemaphore.h
    include/CMclSharedMemory.h
    include/CMclThread.h
    include/CMclWaitableCollection.h
    include/CMclWaitableObject.h
)

add_library(Mcl STATIC ${Main_SRC})

if (MSVC)
    add_definitions(-D_CRT_SECURE_NO_WARNINGS)
endif()
