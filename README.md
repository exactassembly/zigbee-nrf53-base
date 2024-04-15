# Purpose

This project targets ZephyrOS on Nordic nRF53 devices with Zigbee protocol using nRF Connect for Desktop SDK and Toolchain to build and flash.


## Toolchain

This firmware compiles with the following toolsets and versions.

* nRF Connect Command Line Tools Version > 10.24.1 https://www.nordicsemi.com/Products/Development-tools/nRF-Command-Line-Tools/Download
* Segger J-Link Driver Version > 7.96d https://www.segger.com/downloads/jlink/
* nRF Connect Desktop Version > 4.4.1 https://www.nordicsemi.com/Products/Development-tools/nRF-Connect-for-Desktop
* Toolchain Manager Version > v1.4.0
* nRF Connect SDK Version > v2.6.0
* VS Code Version > 1.88.0
* nRF Connect for VS Code Extension Version > v2023.11.3
* Zephyr version: 3.5.99
* Slicon Labs CP210x USB to UART Bridge VCP Driver https://www.silabs.com/developers/usb-to-uart-bridge-vcp-drivers

## Setup

1. Download and install nRF Connect for Desktop.
	- Open Toolchain Manager. Select latest SDK (current version nRF Connect SDK v2.6.0).
2. Download and nRF Connect Command Line Tools (current version 10.24.1).
3. Download and install Segger J-Link (current version v7.96d).
4. Download and install VS Code (current version 1.88.0). Install appropriate extension packs to build and edit code...
5. Open VS Code:
	- Select Extesnsions icon from lefthand toolbar.
	- Install nRF Connect for VS Code 
	- Install nRF Connect for VS Code Extensions
	- When in doubt, refer to the [nRF Connect for VS Code website](https://www.nordicsemi.com/Products/Development-tools/nRF-Connect-for-VS-Code/) from Nordic and follow the "Installation" video.
6. Download and install Silicon Labs VCP drivers (needed for UART serial terminal).

## Pre Build 

Clone GitHub repository into your local worksapce directory. https://github.com/exactassembly/zigbee-nrf53-base.git

## Build

1. Select the nRF Connect tool icon from the menu on the left.
2. From the WELCOME menu in NRF CONNECT:
	- Select "Manage toolchains": Verify v2.6.0 is installed and set to active toolchain.
	- Select "Manage SDK's": Verify v2.6.0 is installed and set to active SDK
	- Select "Open an existing application": Select the folder with the application.
3. Under the APPLICATIONS menu select "Add build configuration".
4. From the dropdaown menu on the build window select "nrf5340dk_nrf5340_cpuapp"
5. Leave all defaults and select the "Build Configuration" button.

## Flash

1. Connect J-Link JTag probe to header on development kit.
2. From nRF Connect SDK toolbar, select "Flash".

### Useful Hints:

* If board becomes unresponsive or produces fatal errors:
	- From GitBash Terminal:
		- nrfjprog --help
		- nrfjprog --revover
		- rnfjprog --eraseall

