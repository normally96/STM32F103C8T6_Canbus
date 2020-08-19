################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Startup/subdir.mk
-include Src/subdir.mk
-include Drivers/STM32F1xx_HAL_Driver/Src/subdir.mk
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
canbus_receive.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
canbus_receive.list \

OBJCOPY_BIN += \
canbus_receive.bin \


# All Target
all: canbus_receive.elf secondary-outputs

# Tool invocations
canbus_receive.elf: $(OBJS) $(USER_OBJS) G:\workspace\stm32\canbus_receive\STM32F103C8TX_FLASH.ld
	arm-none-eabi-gcc -o "canbus_receive.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"G:\workspace\stm32\canbus_receive\STM32F103C8TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="canbus_receive.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

canbus_receive.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "canbus_receive.list"
	@echo 'Finished building: $@'
	@echo ' '

canbus_receive.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "canbus_receive.bin"
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
