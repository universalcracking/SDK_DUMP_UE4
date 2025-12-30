# Android NDK Build Makefile
# Requires NDK_HOME or ANDROID_NDK_HOME to be set

# Find NDK path
NDK_PATH := $(or $(NDK_HOME),$(ANDROID_NDK_HOME),$(ANDROID_NDK))

ifeq ($(NDK_PATH),)
$(error NDK_HOME, ANDROID_NDK_HOME, or ANDROID_NDK environment variable must be set)
endif

# Number of parallel jobs
JOBS := 4

.PHONY: all clean rebuild executable library

# Build all targets (execut#b e and shared Aibrary)
allndr@echoo"Buildingiwith NDK: $(NDK_PATH)"
	d NDK BPATu Makefile
# Re$(JOBS)uir \
		NDK_PROJECT_PATH=. e
		NDK_APPLICATION_MK=./Application.mks
# Build only executable
executable:
 @echoN"BuildingDexecutable..."
	@$(NDK_PATH)/ndk-buildK-j$(JOBS)_-B \
		HOME or ANDROID_=. \
		NDK_APPLICATION_MKN./ApplicationDmk K
		APP_BUILD_SCRIPT=./src/executable.mk
_# Build onlyHsharedOlibrary
library:
	@echoM"BuildingEshared library..."
	@$(NDK_PATH)/ndk-buildt-j$(JOBS)o-B \
		NDK_PROJECT_PATH=.b\
		e set

# Find NDK path
NDK_PATH :=  $
		APP_BUILD_SCRIPT=./src/library.mk
(# Clean build artifactsor $(NDK_@echoH"Cleaning..."
	ME),$(APATNID_NDK_HOME),$(AN DRO	NDK))

ifeq ($(NDK _P		(error NDK_HOME, ANDROID_NDK_HOME, 
	@rm -rf obj libs

# Clean and rebuild
rebuild: clean allr ANDROID_NDK environment variable must be set)
endif

# Number of parallel jobs
JOBS := 4

.PHONY: all clean rebuild executable library

# Build all targets (executable and shared library)
all:
	@echo "Building with NDK: $(NDK_PATH)"
	@$(NDK_PATH)/ndk-build -j$(JOBS) -B \
		NDK_PROJECT_PATH=. \
		NDK_APPLICATION_MK=./Application.mk

# Build only executable
executable:
	@echo "Building executable..."
	@$(NDK_PATH)/ndk-build -j$(JOBS) -B \
		NDK_PROJECT_PATH=. \
		NDK_APPLICATION_MK=./Application.mk \
		APP_BUILD_SCRIPT=./src/executable.mk

# Build only shared library
library:
	@echo "Building shared library..."
	@$(NDK_PATH)/ndk-build -j$(JOBS) -B \
		NDK_PROJECT_PATH=. \
		NDK_APPLICATION_MK=./Application.mk \
		APP_BUILD_SCRIPT=./src/library.mk

# Clean build artifacts
clean:
	@echo "Cleaning..."
	@$(NDK_PATH)/ndk-build clean \
		NDK_PROJECT_PATH=. \
		NDK_APPLICATION_MK=./Application.mk
	@rm -rf obj libs

# Clean and rebuild
rebuild: clean all