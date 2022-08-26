# Data-Acquisition-System-Project

## Phase 1: Project Requirement
  a. Project abstract Preparation.  
  b. Setup Embedded Linux Development Environment.

## Phase 2: Add LM35 Temperature sensor & EEPROM on target board
###  Step 1: Study Phase
          a. High Level Analysis:-  Understand Basics/terminology of ADC controller & EEPROM and prepare a document.
                                    Project Deliverable: Basics Document
          b. Low Level Analysis:-   Study ADC controller in AM3358 Technical Reference Manual and undestood the below things.
                                    ADC controller specifications.
                                    ADC Functional Block Diagram.
                                    ADC Controller Register Programming model.
                                    Identify LM35 interface with ADC channel with the help of schematic diagram.
                                    Understood EEPROM Write I2C comunication protcol format.
                                    Prepare ADC-AM3358 Functional Block diagram.
                                    Prepare EEPROM-AM3358 Functional Block diagram.
          Project Deliverable : Document
###  Step 2: Implementation
          a. Bootloader stage:- Enable ADC & I2C1 controller mux configuration and clock in u-boot source code.
          b. Kernel stage:- DTS Modification:
                            Add ADC device controller mux configuration if needed, base address, interrupt number 
                            and low level device driver compatibility name in device tree source code. 
                            Add EEPROM I2C1 slave information in device tree source code.
          Project Deliverable: patch
          
          Driver Modifications: Identify ADC and  EEPROM I2C slave low level driver and find out low level driver comes which Linux subsystem. 
          Project Deliverable: patch
  
###  Step 3: Application

          Write an application to read temperature value in digital format and convert in to degree centigrade format.
          Write an EEPROM test application to store temperature value in to EEPROM.

## Phase 3: Integration

          Write a self-diagnostic test application to integrate all the peripherals and test the drivers.
          Project Deliverable: application
