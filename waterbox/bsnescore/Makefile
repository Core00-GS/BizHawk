NEED_LIBCO := 1

CXXFLAGS := -std=c++17 \
	-I../libco -I./bsnes \
	-Werror=int-to-pointer-cast \
	-Wno-parentheses -Wno-sign-compare -Wno-unused-variable -Wno-trigraphs -Wno-switch -Wno-reorder -Wno-misleading-indentation \
	-Wno-unqualified-std-cast-call -Wno-mismatched-tags -Wno-overloaded-virtual -Wno-bitwise-instead-of-logical \
	-fno-threadsafe-statics -fno-strict-aliasing -fwrapv

CCFLAGS := -std=c11 -DGB_INTERNAL -DGB_DISABLE_DEBUGGER -DGB_DISABLE_CHEATS -DGB_DISABLE_TIMEKEEPING -DGB_DISABLE_REWIND -D_GNU_SOURCE -DGB_VERSION= \
	-Wall -Wextra -Wno-unused-parameter -Wno-sign-compare -Wno-missing-braces -Wno-missing-field-initializers

TARGET = bsnes.wbx

SRCS_PROCESSORS = \
	$(ROOT_DIR)/bsnes/processor/spc700/spc700.cpp \
	$(ROOT_DIR)/bsnes/processor/wdc65816/wdc65816.cpp \
	$(ROOT_DIR)/bsnes/processor/arm7tdmi/arm7tdmi.cpp

SRCS_EMULATOR = \
	$(ROOT_DIR)/bsnes/emulator/emulator.cpp

SRCS_GB = \
	$(ROOT_DIR)/bsnes/gb/Core/apu.c \
	$(ROOT_DIR)/bsnes/gb/Core/camera.c \
	$(ROOT_DIR)/bsnes/gb/Core/rumble.c \
	$(ROOT_DIR)/bsnes/gb/Core/display.c \
	$(ROOT_DIR)/bsnes/gb/Core/gb.c \
	$(ROOT_DIR)/bsnes/gb/Core/joypad.c \
	$(ROOT_DIR)/bsnes/gb/Core/mbc.c \
	$(ROOT_DIR)/bsnes/gb/Core/memory.c \
	$(ROOT_DIR)/bsnes/gb/Core/printer.c \
	$(ROOT_DIR)/bsnes/gb/Core/random.c \
	$(ROOT_DIR)/bsnes/gb/Core/save_state.c \
	$(ROOT_DIR)/bsnes/gb/Core/sgb.c \
	$(ROOT_DIR)/bsnes/gb/Core/sm83_cpu.c \
	$(ROOT_DIR)/bsnes/gb/Core/timing.c

SRCS_SFC = \
	$(ROOT_DIR)/bsnes/sfc/interface/interface.cpp \
	$(ROOT_DIR)/bsnes/sfc/system/system.cpp \
	$(ROOT_DIR)/bsnes/sfc/controller/controller.cpp \
	$(ROOT_DIR)/bsnes/sfc/cartridge/cartridge.cpp \
	$(ROOT_DIR)/bsnes/sfc/memory/memory.cpp \
	$(ROOT_DIR)/bsnes/sfc/cpu/cpu.cpp \
	$(ROOT_DIR)/bsnes/sfc/smp/smp.cpp \
	$(ROOT_DIR)/bsnes/sfc/dsp/dsp.cpp \
	$(ROOT_DIR)/bsnes/sfc/ppu/ppu.cpp \
	$(ROOT_DIR)/bsnes/sfc/ppu-fast/ppu.cpp \
	$(ROOT_DIR)/bsnes/sfc/expansion/expansion.cpp \
	$(ROOT_DIR)/bsnes/sfc/coprocessor/coprocessor.cpp \
	$(ROOT_DIR)/bsnes/sfc/slot/slot.cpp \
	$(ROOT_DIR)/bsnes/target-bsnescore/bsnescore.cpp

SRCS = $(SRCS_PROCESSORS) $(SRCS_EMULATOR) $(SRCS_GB) $(SRCS_SFC)

include ../common.mak
