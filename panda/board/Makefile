PROJ_NAME = panda
CFLAGS = -g -Wall -Wextra -Wstrict-prototypes -Werror

CFLAGS += -mlittle-endian -mthumb -mcpu=cortex-m4
CFLAGS += -mhard-float -DSTM32F4 -DSTM32F413xx -mfpu=fpv4-sp-d16 -fsingle-precision-constant
dp_hkg := $(shell cat /data/params/d/dp_hkg)
$(info dp_hkg is ${dp_hkg})
ifeq ($(dp_hkg), 1)
  CFLAGS += -Dhkg
endif
STARTUP_FILE = startup_stm32f413xx

include build.mk
