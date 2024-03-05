---
title: Chimera Demo
nav_order: 1
---

[![MCHP](https://www.microchip.com/ResourcePackages/Microchip/assets/dist/images/logo.png)](https://www.microchip.com) 
# MPLAB® Harmony 3 Wireless

# DemoStore for Chimera
Chimera curiosity board is programmed with a default application. If a customer wants to run another demo, instead of going through regular ways of using MPLABX/MPLAB IPE, he can use DemoStore Concept to reprogram with another
demo. DemoStore Concept is realized with the following
 - MBD App
 - DemoStoreConcept Utility 
 
 MBD App can be used to upgrade firmware in curiosity board if the exiting demo in curiosity board supports OTA DFU. Zigbee only demo can be programmed using MBD app if the previous program supports OTA DFU but 
 other demo application can't be programmed if the previous program is doesn't support OTA DFU.
 DemoStoreConcept Utility doesn't have any such restriction. Any available demo application can be programmed into Chimera curiosity board but MPLABX IPE needs to be installed on the PC and Chimera Curiosity  
 board needs to be connected to PC through USB.
 OTA DFU + MBD app in under progress and will be available early next year.
 
## Hardware Requirement
 - Chimera curiosity board
 - USB cable
 - PC
## Software
 - Microchip Data App(MBD)
 - iOS/Android device
 - MPLabX IDE/IPE
 - Latest Chimera Release 
 - DemoStoreConcept C# Utility
Following demo's are available

# BLE Building Block Demo

## Connection(Central)
This application demonstrate users to enable scan and connect functionality on the BLE Central Device (WBZ45x). For a successful BLE connection, ADVERTISER must start sending advertisement packets on the three primary
advertisement channels (or a subset of these channels). This allows the devices scanning for advertisers to find then and read their advertisement data, the scanner can initiate a connection if advertiser allows it. 
To demonstrate a BLE Connection on WBZ45x, two devices needed. [here is the code](./ble_central_conn_wbz451_curiosity.hex)

## Legacy Scan(Central)
This Application Example enables users to do passive scanning. After programming the Application Example, on reset user will be able to see the beginning of scan operation, the Bluetooth addresses of devices
scanned for the next 10 seconds. [Here is the code](./ble_legacy_scan_wbz451_curiosity.hex)

## BLE Scanning Extended Advertisements(Central)
This application will enable scanning of Extended Advertisements (ADV_EXT_IND, ADV_AUX_IND) on WBZ451 Curiosity board. For a successful scan of Extended Advertisement user needs to have a broadcaster
transmitting these Advertisements. In BLE a central or observer always starts with scanning.[Here is the code](./ble_scan_ext_adv_wbz451_curiosity.hex)

## BLE Transparent UART(Central)
This application demonstrates a central device and send/receive characters between 2 connected BLE devices over Microchip proprietary Transparent UART Profile. The central and peripheral devices in this 
demo needs 2 WBZ45x devices. [Here is the code](./ble_central_trp_uart_wbz451_curiosity.hex)

## BLE Multilink Transparent UART(Central)
This application will help users to demonstrate a multilink central device and send/receive characters between connected BLE devices over Microchip proprietary Transparent UART Profile. 
The multilink central will enable users to connect multiple peripheral devices(maximum 6) to a central device. The central and peripheral devices in this application are WBZ45x devices.
[Here is the code](./ble_multilink_central_trp_uart_wbz451_curiosity.hex)

## BLE Connection(Peripheral)
This application will help users to enable advertisements with WBZ451 Curiosity board using BLE Advertisement is Broadcasting of small packets to peer devices. A BLE peripheral device 
always starts with advertisements. Advertisement packets enable a central or observer to discover and connect to a peripheral.
[Here is the code](./peripheral_conn_wbz451_curiosity.hex)

## BLE Extended Advertisements(Peripheral) 
This application demostrate Extended Advertisements (1M, 2M,coded PHY -- 125kbps) on WBZ451 Curiosity Board. This application (ext_adv) enables users to send application data using extended advertisements.
Extended Advertisements are used to send more data than the legacy advertisements allow and allow long range functionality when using Coded PHY. Use of Extended Advertisements also enables the users to select
between different PHYs (1M, 2M and **LE Coded**) which are not permitted when using legacy advertisements. In BLE a peripheral or broadcaster always starts with advertisements. Advertisement packets enable a
central or observer to discover a peripheral or broadcaster. [Here is the code](./ble_ext_adv_wbz451_curiosity.hex)

## BLE Legacy Advertisements(Peripheral)
This Application help users to enable BLE Advertisements on WBZ451 Curiosity board, Broadcasting of small packets to peer devices. A BLE peripheral or broadcaster always starts with advertisements. Advertisement packets
enable a central or observer to discover a peripheral or broadcaster. [Here is the code](./legacy_adv_wbz451_curiosity.hex)

## BLE Transparent UART(Peripheral)
This Application help users to demonstrate a peripheral device and send/receive characters between 2 connected BLE devices over Microchip proprietary Transparent UART Profile. Peripheral device will be WBZ45x Device 
and Central device can either be a Smartphone with Light Blue App or another WBZ45x Device. [Here is  the code](./peripheral_trp_uart_wbz451_curiosity.hex)


# Advance Application

## BLE Sensor DEMO
This application demonstrates the capability of WBZ451 module to connect to a mobile phone through Bluetooth Low Energy(BLE). The RGB LED on the Curiosity board can be controlled by mobile app. 
The WBZ451 device will also report the temperature data periodically to mobile phone through Bluetooth low energy (BLE).

1. The WBZ451 module will be a BLE peripheral device and will advertise on startup. The user can initiate the connection through mobile application.
   
2. Uses "BLE Sensor" from the Microchip Bluetooth Data (MBD) mobile app for BLE demonstration.
   
3. When CONNECTED(ING) to the application the BLUE color "User LED" will turn on.
   
4. From the Phone Application the following actions can be performed.
    - The RGB LED can be switched On/Off from MBD mobile app.
    - When LED is switched On, the RGB color can be changed from mobile app color wheel.
      - The RGB color value is received as HSV (Hue, Saturation, Value) from mobile app through TRPS [transparent profile and service](protocol.md)
      - The HSV value is converted to RGB equivalent value in the device. The corresponding PWM duty cycle for R,G,B will be calculated and the PWM pulse is provided on R,G,B LEDs.
5. From the  WBZ451 module the following actions can be performed.
    - The RGB LED can be switched On/Off by pressing the On board "User Button".
      - When the "User Button" is pressed and released RGB LED is switched ON with default color GREEN or the last stored color.
      - When the "User Button" is pressed and released again, then the RGB LED will be toggled from the previous state.
    - Read the temperature sensor every 1 sec once and send the temperature value to mobile app when the temperature changes about 1 degree C.
[Here is the code](./ble_sensor_app_v0.7.2.1.hex)

## BLE UART Demo
BLE UART Application demonstrate several functionalities including:
1.	Connection with mobile phone via BLE
2.	Data transmission between PIC32CX-BZ and mobile phone via BLE and throughput evaluation.
3.	Data transmission between PIC32CX-BZ and mobile phone via BLE; data transmission between PIC32CX-BZ and a host device (such as PC) via UART and throughput evaluation.
In order to do the data comparison in the receiver side, the fixed data pattern shall be provided in the sender side.
4. Data transmission for the UART mode or the loopback mode via BLE between PIC32CX-BZ devices which are both the client role of a central device and the server role of a peripheral device.
5. Data exchange between PIC32CX-BZ and mobile phone via BLE long range or Data exchange between PIC32CX-BZ devices via BLE long range and the link loss distance evaluation for long range 
or maximum link distatnce evaluation for long range.
[Here is the code](./ble_uart_app_wbz451_curiosity_board.hex)
# Zigbee Application

## Zigbee Light
This Application describes how to quickly start with the Zigbee Light reference applications on PIC32CX-BZ.
Zigbee is a full-featured, production grade, embedded software development platform from Microchip. 
It provides a framework for creating Zigbee lighting & occupancy and proprietary zigbee devices running on 
supported Microchip microcontrollers and IEEE® 802.15.4-2006-compliant[1] radio transceivers. 

Zigbee Device reference application implements behavior of Zigbee Lighting and Occupancy (ZLO) devices and 
Green power device for operation on a zigbee-PRO network.
The list of Applicaiton device types supported as part of this reference application are as follows,
1. Combined Interface( Gateway / Coordinator)
2. Light devices (OnOff  / Dimmable / Color / Extended Color / Temperature Color Light)
3. Thermostat
4. Color scene controller
5. Multi Sensor
6. Intruder Alarm System(IAS) - ACE
7. Zigbee Green Power - An additional feature which is enabled on top of the above deice types based on its capability.
[Here is the code](./zigbee_ExtendedLight_v1.2E.hex)

## Zigbee Combined Interface/Gateway
This Application demonstrate how to quickly start with the Zigbee COmbined Interface/ Gateway / Coordinator reference applications on PIC32CX-BZ.
Zigbee is a full-featured, production grade, embedded software development platform from Microchip. 
It provides a framework for creating Zigbee lighting & occupancy and proprietary zigbee devices running on 
supported Microchip microcontrollers and IEEE® 802.15.4-2006-compliant[1] radio transceivers. 

Zigbee Device reference application implements behavior of Zigbee Lighting and Occupancy (ZLO) devices and 
Green power device for operation on a zigbee-PRO network.
The list of Applicaiton device types supported as part of this reference application are as follows,
1. Combined Interface( Gateway / Coordinator)
2. Light devices (OnOff  / Dimmable / Color / Extended Color / Temperature Color Light)
3. Thermostat
4. Color scene controller
5. Multi Sensor
6. Intruder Alarm System(IAS) - ACE
7. Zigbee Green Power - An additional feature which is enabled on top of the above deice types based on its capability.
[Here is the code](./zigbee_CombinedInterface_v1.2E.hex)

## Multiprotocol (BLE+ZIGBEE) Concurrent Application
This application will help users to demonstrate multiprotocol (BLE+ZIGBEE). Light can be controlled from MBD app as well as through Zigbee.
[Here is the code](./ble_zigbee_basic.X.production.hex)
## WBZ451 Multiprotocol Application Demo
This application demonstrates the multi-protocol (concurrent operation of both Zigbee and BLE stacks) functionality of PIC32CXBZ family of devices and modules. The Zigbee commissioning over BLE uses 
Bluetooth Low Energy (BLE) link to exchange Zigbee commission data and run both Zigbee and BLE tasks simultaneously under FreeRTOS. The local zigbee lights (on board RGB LED) can be controlled over BLE or from Zigbee network.
Multi-protocol can also be referred as "combo" for ease of readability in this doc.
[Here is the code](./ble_zigbee_light_prov_v0.1.0.2.hex)

