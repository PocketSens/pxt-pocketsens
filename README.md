PocketSens for micro:bitPocketSens is an ultimate, all-in-one micro:bit expansion board designed for STEM educators and makers by WiseLife Technology. This MakeCode extension provides custom blocks to easily interface with the onboard I2C sensors, power management, and expansion ports without the hassle of messy wiring.FeaturesPlug & Play: No soldering or breadboards required.Onboard Sensors: Integrated Temperature, Humidity, and Ambient Light sensors.Robust Design: Classroom-ready enclosure to protect the PCB and battery.MakeCode Ready: Fully compatible with Microsoft MakeCode.Adding the Extension in MakeCodeTo use this extension, you need to add it to your MakeCode project:Go to MakeCode for micro:bitClick on New ProjectClick on Extensions under the gearwheel menuSearch for https://github.com/pocketsens/pxt-pocketsens and import it.Block Usage Examples1. Reading the TemperatureUse the read temperature block to get the current ambient temperature in Celsius.basic.forever(function () {
    basic.showNumber(PocketSens.readTemperature())
})
2. Checking the Light LevelEasily trigger events based on classroom lighting conditions.basic.forever(function () {
    if (PocketSens.readLightLevel() < 50) {
        basic.showIcon(IconNames.No)
    } else {
        basic.showIcon(IconNames.Yes)
    }
})
Hardware Pinout ReferenceFor advanced users and MicroPython programming, here is the hardware I2C and IO pin mapping:Featuremicro:bit PinNoteI2C SDAP20Shared I2C bus for all sensorsI2C SCLP19Shared I2C bus for all sensorsExpansion GVS 1P0Analog/DigitalExpansion GVS 2P1Analog/DigitalSupported Targetsfor PXT/microbit
(The metadata above is needed for MakeCode to correctly index this extension.)LicenseMIT License. Copyright (c) 2026 WiseLife Technology Co., Ltd.
