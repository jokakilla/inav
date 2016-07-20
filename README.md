# INAV

![INAV](http://static.rcgroups.net/forums/attachments/6/1/0/3/7/6/a9088858-102-inav.png)

Flight Controller software for STM32 microcontrollers

## Important: PID values and scaling

Starting at iNav 1.2 release (and current master) INAV uses the same scaling for PIDs as Cleanflight/Betaflight LuxFloat and MWRewrite PID controllers. That means the following:

* PIDs from CF/BF can be used in INAV, no need to retune for INAV
* INAV uses the same PID defaults that Cleanflight and Betaflight
* Current INAV tunes can be converted to new using [this guide](https://github.com/iNavFlight/inav/wiki/PID-conversion-from-pre-1.2-to-1.2). This applies to all INAV 1.1 users

## Features

* Runs on STM32F1 and STM32F3 processors
* Supported boards:
    * Naze32/Flip32 (STM32F1, I2C sensors)
    * Seriously Pro Racing F3 (STM32F303, I2C sensors, large flash, excellent I/O.)
    * TauLabs Sparky (STM32F303, I2C sensors, based board with acc/gyro/compass and baro)
    * OpenPilot CC3D (STM32F103, SPI acc/gyro)
    * Seriously Dodo (STM32F3)
    * FuryF3 (STM32F3, SPI acc/gyro)
    * CJMCU nano quadcopter board
    * Developer breakout boards: (Port103R, EUSTM32F103RC, Olimexino, STM32F3Discovery)
    * others
* Advanced GPS and navigation support:
    * Position Hold
    * Return To Home with Land
    * Waypoints
    * Follow Me mode (compatible Ground Station required)
    * RTH on Failsafe
* Support for more than 8 RC channels - (e.g. 16 Channels via FrSky X4RSB SBus).
* Support for N-Position switches via flexible channel ranges
* Multi-color RGB LED Strip support (each LED can be a different color using variable length WS2811 Addressable RGB strips - use for Orientation Indicators, Low Battery Warning, Flight Mode Status, etc)
* Oneshot125 ESC support.
* Blackbox flight recorder logging (to onboard flash or external SD card)
* Floating point PID controller
* Simultaneous Bluetooth configuration and OSD.
* Supported telemetry protocols:
    * LTM
    * FrSky Telemetry
    * SmartPort Telemetry
    * MAVLink (basic support)
    * Graupner HoTT telemetry
* Multiple simultaneous telemetry providers.
* RSSI via ADC - Uses ADC to read PWM RSSI signals, tested with FrSky D4R-II and X8R.
* OLED Displays - Display information on: Battery voltage, profile, rate profile, version, sensors, RC, etc.
* In-flight manual PID tuning and rate adjustment.
* Rate profiles and in-flight selection of them.
* Graupner PPM failsafe.
* Configurable serial ports for Serial RX, Telemetry, MSP, GPS - Use most devices on any port, softserial too.

For a list of features, changes and some discussion please review the thread on MultiWii forums and consult the documentation.

http://www.multiwii.com/forum/viewtopic.php?f=23&t=5149

## Installation

See: https://github.com/iNavFlight/inav/blob/master/docs/Installation.md

## Documentation

There is lots of documentation here: https://github.com/iNavFlight/inav/tree/master/docs

If what you need is not covered then refer to the baseflight documentation. If you still can't find what you need then visit the #iNavflight on the Freenode IRC network

## IRC Support and Developers Channel

There's a dedicated IRC channel here:

irc://irc.freenode.net/#iNavflight

If you are using windows and don't have an IRC client installed then take a look at HydraIRC - here: http://hydrairc.com/

Etiquette: Don't ask to ask and please wait around long enough for a reply - sometimes people are out flying, asleep or at work and can't answer immediately.


## Configuration Tool

To configure INAV you should use the INAV-configurator GUI tool (Windows/OSX/Linux).
Currently you have to download the sourcecode and load into Chrome manually from the github page

https://github.com/iNavFlight/inav-configurator

If you rather just want to use Cleanflight configurator you can download from here:
https://chrome.google.com/webstore/detail/cleanflight-configurator/enacoimjcgeinfnnnpajinjgmkahmfgb


## Contributing

Contributions are welcome and encouraged.  You can contribute in many ways:

* Documentation updates and corrections.
* How-To guides - received help?  help others!
* Bug fixes.
* New features.
* Telling us your ideas and suggestions.

The best place to start is the IRC channel on freenode (see above), drop in, say hi. Next place is the github issue tracker:

https://github.com/iNavFlight/inav/issues

https://github.com/iNavFlight/inav-configurator/issues

Before creating new issues please check to see if there is an existing one, search first otherwise you waste peoples time when they could be coding instead!

## Developers

Please refer to the development section in the [docs/development](https://github.com/iNavFlight/inav/tree/master/docs/development) folder.


## INAV Releases
https://github.com/iNavFlight/inav/releases
