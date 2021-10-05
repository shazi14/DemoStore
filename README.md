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
# BLE Building Block Demo(Central)
## Connection
This application demonstrate users to enable scan and connect functionality on the BLE Central Device (WBZ45x). For a successful BLE connection, ADVERTISER must start sending advertisement packets on the three primary
advertisement channels (or a subset of these channels). This allows the devices scanning for advertisers to find then and read their advertisement data, the scanner can initiate a connection if advertiser allows it. 
To demonstrate a BLE Connection on WBZ45x, two devices needed. [here is the code](./ble_central_conn_wbz451_curiosity.X.production.hex)
## Legacy Scan
This Application Example enables users to do passive scanning. After programming the Application Example, on reset user will be able to see the beginning of scan operation, the Bluetooth addresses of devices
scanned for the next 10 seconds. [Here is the code](./ble_legacy_scan_wbz451_curiosity.X.production.hex)
## BLE Scanning Extended Advertisements
This application will enable scanning of Extended Advertisements (ADV_EXT_IND, ADV_AUX_IND) on WBZ451 Curiosity board. For a successful scan of Extended Advertisement user needs to have a broadcaster
transmitting these Advertisements. In BLE a central or observer always starts with scanning.[Here is the code](./ble_scan_ext_adv_wbz451_curiosity.X.production.hex)
## BLE Transparent UART(Central)
This application demonstrates a central device and send/receive characters between 2 connected BLE devices over Microchip proprietary Transparent UART Profile. The central and peripheral devices in this 
demo needs 2 WBZ45x devices. [Here is the code](./ble_central_trp_uart_wbz451_curiosity.X.production.hex)
## BLE Multilink Transparent UART(Central)
This application will help users to demonstrate a multilink central device and send/receive characters between connected BLE devices over Microchip proprietary Transparent UART Profile. 
The multilink central will enable users to connect multiple peripheral devices(maximum 6) to a central device. The central and peripheral devices in this application are WBZ45x devices.
[Here is the code](./ble_multilink_central_trp_uart_wbz451_curiosity.X.production.hex)
## BLE Connection(Peripheral)
This application will help users to enable advertisements with WBZ451 Curiosity board using BLE Advertisement is Broadcasting of small packets to peer devices. A BLE peripheral device 
always starts with advertisements. Advertisement packets enable a central or observer to discover and connect to a peripheral.
[Here is the code](./peripheral_conn_wbz451_curiosity.X.production.hex)
## BLE Extended Advertisements 
This application demostrate Extended Advertisements (1M, 2M,coded PHY -- 125kbps) on WBZ451 Curiosity Board. This application (ext_adv) enables users to send application data using extended advertisements.
Extended Advertisements are used to send more data than the legacy advertisements allow and allow long range functionality when using Coded PHY. Use of Extended Advertisements also enables the users to select
between different PHYs (1M, 2M and **LE Coded**) which are not permitted when using legacy advertisements. In BLE a peripheral or broadcaster always starts with advertisements. Advertisement packets enable a
central or observer to discover a peripheral or broadcaster. [Here is the code](./ble_ext_adv_wbz451_curiosity.X.production.hex)
## BLE Legacy Advertisements
This Application help users to enable BLE Advertisements on WBZ451 Curiosity board, Broadcasting of small packets to peer devices. A BLE peripheral or broadcaster always starts with advertisements. Advertisement packets
enable a central or observer to discover a peripheral or broadcaster. [Here is the code](./legacy_adv_wbz451_curiosity.X.production.hex)
## BLE Transparent UART(Peripheral)
This Application help users to demonstrate a peripheral device and send/receive characters between 2 connected BLE devices over Microchip proprietary Transparent UART Profile. Peripheral device will be WBZ45x Device 
and Central device can either be a Smartphone with Light Blue App or another WBZ45x Device. [Here is  the code](./peripheral_trp_uart_wbz451_curiosity.X.production.hex)

