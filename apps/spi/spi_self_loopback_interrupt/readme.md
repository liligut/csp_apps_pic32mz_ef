[![MCHP](https://www.microchip.com/ResourcePackages/Microchip/assets/dist/images/logo.png)](https://www.microchip.com)

# SPI interrupt

This example application demonstrates how to use the SPI peripheral to transmit and receive a block of data using interrupt.

## Description

This example shows the transmit and receive operation over a SPI interface in a non-blocking manner. The peripheral interrupt is used to manage the transfer.The example application transmits known values from an array and verifies the data received through the loop back by comparing the transmitted data and the received data. The example application performs the loop back test only once after a power on reset. After the loop back is complete, the status of the loop back is indicated and the application remains idle. The loop back test requires the MOSI output pin to be connected to the MISO input pin so that anything transmitted will also be received.

## Downloading and building the application

To download or clone this application from Github, go to the [top level of the repository](https://github.com/Microchip-MPLAB-Harmony/csp_apps_pic32mz_ef) and click

![clone](../../../docs/images/clone.png)

Path of the application within the repository is **apps/spi/spi_self_loopback_interrupt/firmware** .

To build the application, refer to the following table and open the project using its IDE.

| Project Name      | Description                                    |
| ----------------- | ---------------------------------------------- |
| pic32mz_ef_sk.X | MPLABX project for [PIC32MZ Embedded Connectivity with FPU (EF) Starter Kit](https://www.microchip.com/DevelopmentTools/ProductDetails/dm320007) |
|||

## Setting up the hardware

The following table shows the target hardware for the application projects.

| Project Name| Board|
|:---------|:---------:|
| pic32mz_ef_sk.X | [PIC32MZ Embedded Connectivity with FPU (EF) Starter Kit](https://www.microchip.com/DevelopmentTools/ProductDetails/dm320007) |
|||

### Setting up [PIC32MZ Embedded Connectivity with FPU (EF) Starter Kit](https://www.microchip.com/DevelopmentTools/ProductDetails/dm320007)

- Use a jumper wire to short pin 7 and pin 37 of the J12 connector
- Connect the Debug USB port on the board to the computer using a micro USB cable

## Running the Application

- Build and program the application using its IDE
- LED indicates the success or failure:
  - LED is turned ON when the when the value received matched with the transmitted value
  - LED is turned OFF when the when the value received did not match with the transmitted value

Following table provides LED names:

| Board | LED name |
| ----- | -------- |
| [PIC32MZ Embedded Connectivity with FPU (EF) Starter Kit](https://www.microchip.com/DevelopmentTools/ProductDetails/dm320007) | LED1|
|||