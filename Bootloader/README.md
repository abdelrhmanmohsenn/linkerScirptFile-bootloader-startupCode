# STM32F407VG Bootloader 

This repository contains the implementation of a bootloader for the STM32F407VG microcontroller. The bootloader allows users to perform various operations such as firmware updates, memory read/write, flash erase, and more.

## Introduction

The bootloader provided here is designed for the STM32F407VG microcontroller. It allows users to communicate with the device via a serial communication interface (UART) and perform essential operations such as updating firmware, erasing flash memory, and reading memory contents.

## Features

- **UART Communication**: Communication interface with the host device is established using UART.
- **Flash Memory Operations**: Support for erasing flash memory sectors and writing data into flash memory.
- **Read Protection Level**: Ability to read the current flash read protection level.
- **Jump to Address**: Capability to jump to a specified address within the device memory.
- **Command-Line Interface**: Host commands are interpreted through a command-line interface.
- **Error Handling**: Comprehensive error handling mechanisms ensure safe operation.

## Getting Started

To use the bootloader, follow these steps:

1. Clone this repository to your development environment.
2. Include the `bootloader.h` file in your project.
3. Implement the required hardware interfaces for UART communication.
4. Customize the bootloader functionalities as per your requirements.
5. Build and flash the bootloader firmware onto your STM32F407VG device.

## Usage

To use the bootloader, establish a serial communication link between your host device and the STM32F407VG microcontroller using a terminal program. Send commands supported by the bootloader to perform various operations.

## Supported Commands

The following commands are supported by the bootloader:

- `GET_VER`: Get the bootloader version.
- `GET_HELP`: Get a list of supported commands.
- `GET_CID`: Get the chip identification number.
- `GET_RDP_STATUS`: Get the read protection level of the flash memory.
- `GO_TO_ADDR`: Jump to a specified address.
- `FLASH_ERASE`: Erase flash memory sectors.
- `MEM_WRITE`: Write data into different memories of the microcontroller.
- `ED_W_PROTECT`: Enable or disable write protection on different sectors of the user flash.
- `MEM_READ`: Read data from different memories of the microcontroller.
- `READ_SECTOR_STATUS`: Read the sector protection status.
- `OTP_READ`: Read the One-Time Programmable (OTP) contents.
- `CHANGE_ROP_LEVEL`: Change the read protection level of the user flash.

For detailed usage instructions for each command, refer to the source code documentation.
