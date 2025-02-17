# Powering On

This document introduces different ways to power your LattePanda. It will cover the input specification, what you will need, and installation steps.


## Overview

**4 Ways to power your Alpha:**

1. Official PD adapter comes with LattePanda Alpha
2. External PD power bank
3. [12 volts input from JST PH2.0 - 4P connector][1]
4. [Lipo battery from 10p power connector][2]

**Discussion about power supply on Forum:**

* <a href="https://www.lattepanda.com/topic-f23t17507.html" target="_blank">Forum Discussion - Suggest a on/off/reset button for Alpha</a>

[1]: /content/alpha_edition/powering/#jst-4p-dc-input-connector
[2]: /content/alpha_edition/powering/#lipo-battery-connector

## Type-C PD Adapters and Battery Banks

### Input Power Specification

* Accepts devices with 45W output (Up to 36 watts will be good enough actually.)

### What You Will Need

* USB Type C Power Delivery power supply or battery

### Installation Steps

1. Connect the USB Type C power supply to the outlet.
2. Connect the USB Type C connector to the LattePanda Alpha USB Type C port or to an attached USB Type C hub with Power Delivery pass through.

### Recommended Power Banks

* <a href="https://www.amazon.com/dp/B07CMLVR6C/ref=cm_sw_r_cp_api_i_R.njCbAT06DNT" target="_blank">Omars 20000 mAh battery.</a>
* <a href="https://www.lattepanda.com/topic-f23t17787.html" target="_blank">More options recommended and tested</a> by ccs_hello (community member).
* Or any other brand power bank supporting PD protocol with up to 36 watts output

## JST 4p DC Input Connector

!!! warning
    Please  make sure that the positive and negative pins are connected correctly! Double check the power connection before powering the system. 

The voltage range of Alpha power input connector is 10~15 volts. So if you're choosing the lipo battery, it should be 3~4 cells. The standard power source is 3A @ 12 volts. The booting power is like 10 watts. And operation power is like 5 watts without much load.

<center>![DC Input Port](/assets/images/DC_Input_Port_Alpha.jpg)</center>
### Input Specification

* 10-15 volts
* Up to 36 watts is recommended 
* Standard power - 3A @ 12 volts
* JST PH2.0 - 4p connector (pin mapping is marked on the board also: -- DC ++, which means two negative pins and two positive pins)

You can check the [details about pinout diagram][5].

[5]: /content/alpha_edition/io_playability/

## Lipo Battery Connector

!!! warning
    Please make sure that 10 pin sequence of the Lipo battery is connected correctly. **Many vendors provide Lipo battery with 10pin connector in the market. It means you may need to change pins' sequence carefully based on the battery you purchased!**

    And wrong power connection will definitely break for LattePanda Alpha!!!

<center>![10 Pin (10p) Battery Connector (Alpha Version Only)](/assets/images/Battery_Connector_Port_Alpha.jpg)</center>

### Recommended Batteries

We haven't officially released battery list that support LattePanda Alpha yet. Somehow shipping batteries around the world is not easy. And it's even hard to find a standard battery for global users. 
But You can check the <a href="https://www.lattepanda.com/topic-f13t16675.html?hilit=battery&start=31" target="_blank">forum discussion about this topic.</a>. Community members already find some alternatives from local battery vendors.

!!! tips
    This 10-pin Li-Po in connector is meant for well-protected (BMS + balancer at minimum) battery pack, not for raw Li-Po/Li-Ion/LiFePO4 cells.   
    (e.g., latter setup will drain below the minimum Li-Po cell voltage which will significantly/irreversibly degrade the life expectancy of cell.)
    Also charging without proper CI (then later CV) charging circuit is outright dangerous.
    <a href="https://www.lattepanda.com/topic-p26725.html" target="_blank">Check details from original post</a> shared by community member ccs_hello

### Input Specification
* **7.4 - 8.2 V**, means 2-cell Lipo battery
* Recommend at least 5 Ah battery
* Lipo battery must be able to charge at a CCCV rating of 1.9! Please check battery specification for charging current before using the battery. 
* Feel free to post your commit or suggestion via <a href="https://github.com/LattePandaTeam/Docs" target="_blank">Github official repo.</a>

### Drawing and Pin Diagram

Molex 10p Panelmate Connector
<center>![10p Drawing](/assets/images/Battery_Connector_Drawing_Alpha.jpg)</center>
<center>![10p Diagram](/assets/images/Battery_Connector_Pin_Diagram_Alpha.jpg)</center>
### Installation Steps

1. Align the 10p battery connector with the LattePanda Alpha battery connector. Make sure the positive red wires align with pins 1-3 on the diagram above.
2. Connect the 10p battery connector to the LattePanda Alpha battery connector.

### Considerations When Using Battery Connector

When using only the 10p battery connector to power LattePanda Alpha, the red and blue initializing lights will not turn on. Hold the power button for 3 seconds and the LattePanda Alpha will boot.


!!! warning
    Only recommended for advanced makers, who have enough hardware experience...

## Related Links
* [Getting Started](/content/alpha_edition/powering/)
* [Hardware Interface](/content/alpha_edition/io_playability/)

**Enjoy your new LattePanda!**

Want to play IoT? Want to study programming? Want to control the physical world? [Check tools recommended first!][4]

[4]: /content/alpha_edition/ide/
