################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32F4xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
stm32-nucleo-ledcontrol.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
stm32-nucleo-ledcontrol.list \

OBJCOPY_BIN += \
stm32-nucleo-ledcontrol.bin \


# All Target
all: stm32-nucleo-ledcontrol.elf secondary-outputs

# Tool invocations
stm32-nucleo-ledcontrol.elf: $(OBJS) $(USER_OBJS) /home/huypn12/Sources/Repos/stm32-nucleo64-kata/stm32-nucleo-ledcontrol/STM32F446RETX_FLASH.ld
	arm-none-eabi-gcc -o "stm32-nucleo-ledcontrol.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"/home/huypn12/Sources/Repos/stm32-nucleo64-kata/stm32-nucleo-ledcontrol/STM32F446RETX_FLASH.ld" --specs=nosys.specs -Wl,-Map="stm32-nucleo-ledcontrol.map" -Wl,--gc-sections -static --specs=nano.specs -mfpu=fpv4-sp-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

stm32-nucleo-ledcontrol.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "stm32-nucleo-ledcontrol.list"
	@echo 'Finished building: $@'
	@echo ' '

stm32-nucleo-ledcontrol.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "stm32-nucleo-ledcontrol.bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_BIN)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
