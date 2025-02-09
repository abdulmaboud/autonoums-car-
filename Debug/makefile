################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include MCAL/TIMER/subdir.mk
-include MCAL/PWM/subdir.mk
-include MCAL/INTERRUPT/subdir.mk
-include MCAL/subdir.mk
-include HAL/USS/subdir.mk
-include HAL/SERVO/subdir.mk
-include HAL/MOTOR/subdir.mk
-include HAL/CLCD/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(ASM_DEPS)),)
-include $(ASM_DEPS)
endif
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

# Add inputs and outputs from these tool invocations to the build variables 
LSS += \
autonomous-car-using-ultrasonic-sensor-atmega32-master.lss \

FLASH_IMAGE += \
autonomous-car-using-ultrasonic-sensor-atmega32-master.hex \

SIZEDUMMY += \
sizedummy \


# All Target
all: autonomous-car-using-ultrasonic-sensor-atmega32-master.elf secondary-outputs

# Tool invocations
autonomous-car-using-ultrasonic-sensor-atmega32-master.elf: $(OBJS) $(USER_OBJS)
	@echo 'Building target: $@'
	@echo 'Invoking: AVR C Linker'
	avr-gcc -Wl,-Map,autonomous-car-using-ultrasonic-sensor-atmega32-master.map -mmcu=atmega32 -o "autonomous-car-using-ultrasonic-sensor-atmega32-master.elf" $(OBJS) $(USER_OBJS) $(LIBS)
	@echo 'Finished building target: $@'
	@echo ' '

autonomous-car-using-ultrasonic-sensor-atmega32-master.lss: autonomous-car-using-ultrasonic-sensor-atmega32-master.elf
	@echo 'Invoking: AVR Create Extended Listing'
	-avr-objdump -h -S autonomous-car-using-ultrasonic-sensor-atmega32-master.elf  >"autonomous-car-using-ultrasonic-sensor-atmega32-master.lss"
	@echo 'Finished building: $@'
	@echo ' '

autonomous-car-using-ultrasonic-sensor-atmega32-master.hex: autonomous-car-using-ultrasonic-sensor-atmega32-master.elf
	@echo 'Create Flash image (ihex format)'
	-avr-objcopy -R .eeprom -R .fuse -R .lock -R .signature -O ihex autonomous-car-using-ultrasonic-sensor-atmega32-master.elf  "autonomous-car-using-ultrasonic-sensor-atmega32-master.hex"
	@echo 'Finished building: $@'
	@echo ' '

sizedummy: autonomous-car-using-ultrasonic-sensor-atmega32-master.elf
	@echo 'Invoking: Print Size'
	-avr-size --format=avr --mcu=atmega32 autonomous-car-using-ultrasonic-sensor-atmega32-master.elf
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) $(FLASH_IMAGE)$(ELFS)$(OBJS)$(ASM_DEPS)$(S_DEPS)$(SIZEDUMMY)$(S_UPPER_DEPS)$(LSS)$(C_DEPS) autonomous-car-using-ultrasonic-sensor-atmega32-master.elf
	-@echo ' '

secondary-outputs: $(LSS) $(FLASH_IMAGE) $(SIZEDUMMY)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
