################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include utilities/subdir.mk
-include startup/subdir.mk
-include source/subdir.mk
-include drivers/subdir.mk
-include device/subdir.mk
-include component/uart/subdir.mk
-include board/subdir.mk
ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

OPTIONAL_TOOL_DEPS := \
$(wildcard ../makefile.defs) \
$(wildcard ../makefile.init) \
$(wildcard ../makefile.targets) \


BUILD_ARTIFACT_NAME := Tp_Integrador
BUILD_ARTIFACT_EXTENSION := axf
BUILD_ARTIFACT_PREFIX :=
BUILD_ARTIFACT := $(BUILD_ARTIFACT_PREFIX)$(BUILD_ARTIFACT_NAME)$(if $(BUILD_ARTIFACT_EXTENSION),.$(BUILD_ARTIFACT_EXTENSION),)

# Add inputs and outputs from these tool invocations to the build variables 

# All Target
all:
	+@$(MAKE) --no-print-directory main-build && $(MAKE) --no-print-directory post-build

# Main-build Target
main-build: Tp_Integrador.axf

# Tool invocations
Tp_Integrador.axf: $(OBJS) $(USER_OBJS) makefile $(OPTIONAL_TOOL_DEPS)
	@echo 'Building target: $@'
	@echo 'Invoking: MCU Linker'
	arm-none-eabi-gcc -nostdlib -L"C:\Users\diazs\Desktop\Programacion escuela\Redes y Protocolos\Sistemas embebidos\curso-lse\lpc845\ejemplos\freertos\Debug" -Xlinker -Map="Tp_Integrador.map" -Xlinker --gc-sections -Xlinker -print-memory-usage -Xlinker --sort-section=alignment -Xlinker --cref -mcpu=cortex-m0plus -mthumb -T Tp_Integrador_Debug.ld -o "Tp_Integrador.axf" $(OBJS) $(USER_OBJS) $(LIBS) -lfreertos
	@echo 'Finished building target: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) Tp_Integrador.axf
	-@echo ' '

post-build:
	-@echo 'Performing post-build steps'
	-arm-none-eabi-size "Tp_Integrador.axf"; # arm-none-eabi-objcopy -v -O binary "Tp_Integrador.axf" "Tp_Integrador.bin" ; # checksum -p LPC845 -d "Tp_Integrador.bin";
	-@echo ' '

.PHONY: all clean dependents main-build post-build

-include ../makefile.targets
