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
canbus_transmit.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
canbus_transmit.list \

OBJCOPY_BIN += \
canbus_transmit.bin \


# All Target
all: canbus_transmit.elf secondary-outputs

# Tool invocations
canbus_transmit.elf: $(OBJS) $(USER_OBJS) G:\workspace\stm32\canbus_transmit\STM32F103C8TX_FLASH.ld
	arm-none-eabi-gcc -o "canbus_transmit.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"G:\workspace\stm32\canbus_transmit\STM32F103C8TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="canbus_transmit.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

canbus_transmit.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "canbus_transmit.list"
	@echo 'Finished building: $@'
	@echo ' '

canbus_transmit.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "canbus_transmit.bin"
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
