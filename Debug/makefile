################################################################################
# Automatically-generated file. Do not edit!
# Toolchain: GNU Tools for STM32 (13.3.rel1)
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include app/src/subdir.mk
-include Drivers/STM32F1xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(S_DEPS)),)
-include $(S_DEPS)
endif
ifneq ($(strip $(S_UPPER_DEPS)),)
-include $(S_UPPER_DEPS)
endif
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

OPTIONAL_TOOL_DEPS := \
$(wildcard ../makefile.defs) \
$(wildcard ../makefile.init) \
$(wildcard ../makefile.targets) \


BUILD_ARTIFACT_NAME := TF_GeneradorDeFunciones_Villegas_Pollero_Rivarola
BUILD_ARTIFACT_EXTENSION := elf
BUILD_ARTIFACT_PREFIX :=
BUILD_ARTIFACT := $(BUILD_ARTIFACT_PREFIX)$(BUILD_ARTIFACT_NAME)$(if $(BUILD_ARTIFACT_EXTENSION),.$(BUILD_ARTIFACT_EXTENSION),)

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
TF_GeneradorDeFunciones_Villegas_Pollero_Rivarola.elf \

MAP_FILES += \
TF_GeneradorDeFunciones_Villegas_Pollero_Rivarola.map \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
TF_GeneradorDeFunciones_Villegas_Pollero_Rivarola.list \


# All Target
all: main-build

# Main-build Target
main-build: TF_GeneradorDeFunciones_Villegas_Pollero_Rivarola.elf secondary-outputs

# Tool invocations
TF_GeneradorDeFunciones_Villegas_Pollero_Rivarola.elf TF_GeneradorDeFunciones_Villegas_Pollero_Rivarola.map: $(OBJS) $(USER_OBJS) C:\Users\mapad\Downloads\tdse-tp2_00-model_integration\TF_GeneradorDeFunciones_Villegas_Pollero_Rivarola\STM32F103RBTX_FLASH.ld makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-gcc -o "TF_GeneradorDeFunciones_Villegas_Pollero_Rivarola.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"C:\Users\mapad\Downloads\tdse-tp2_00-model_integration\TF_GeneradorDeFunciones_Villegas_Pollero_Rivarola\STM32F103RBTX_FLASH.ld" --specs=nosys.specs -Wl,-Map="TF_GeneradorDeFunciones_Villegas_Pollero_Rivarola.map" -Wl,--gc-sections -static -specs=rdimon.specs --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

TF_GeneradorDeFunciones_Villegas_Pollero_Rivarola.list: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "TF_GeneradorDeFunciones_Villegas_Pollero_Rivarola.list"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) TF_GeneradorDeFunciones_Villegas_Pollero_Rivarola.elf TF_GeneradorDeFunciones_Villegas_Pollero_Rivarola.list TF_GeneradorDeFunciones_Villegas_Pollero_Rivarola.map default.size.stdout
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST)

fail-specified-linker-script-missing:
	@echo 'Error: Cannot find the specified linker script. Check the linker settings in the build configuration.'
	@exit 2

warn-no-linker-script-specified:
	@echo 'Warning: No linker script specified. Check the linker settings in the build configuration.'

.PHONY: all clean dependents main-build fail-specified-linker-script-missing warn-no-linker-script-specified

-include ../makefile.targets
