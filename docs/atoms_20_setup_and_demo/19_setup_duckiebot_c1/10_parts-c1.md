# Acquiring the parts for the Duckiebot `C1` {#acquiring-parts-c1 status=ready}

Upgrading your `C0+wjd` configuration to `C1` starts here, with purchasing the necessary components. We provide a link to all bits and pieces that are needed to build a `C1` Duckiebot, along with their price tag. If you are wondering what is the difference between different Duckiebot configurations, read [](#duckiebot-configurations).

In general, keep in mind that:

- The links might expire, or the prices might vary.
- Shipping times and fees vary, and are not included in the prices shown below.
- Buying the parts for more than one Duckiebot makes each one cheaper than buying only one.
- A few components in this configuration are custom designed, and might be trickier to obtain.


<div class='requirements' markdown="1">

Requires: A Duckiebot in `C0+wjd` configuration.

Requires: Cost: USD 77 + Bumpers manufacturing solution

Requires: Time: 21 Days (LED board manufacturing and shipping time)

Results: A kit of parts ready to be assembled in a `C1` configuration Duckiebot.

Next Steps: After receiving these components, you are ready to do some [soldering](#soldering-boards-c1) before [assembling](#assembling-duckiebot-c1) your `C1` Duckiebot.
</div>

## Bill of materials

[//]: #   (<s>[4 Spacers (M3x5)](https://tinyurl.com/y9sjzm4r)</s><s>USD</s>)
[//]: #   (<s>[4 Screws (M3x10)](https://tinyurl.com/y9sjzm4r)</s><s>USD</s>)
<div markdown="1">

 <col2 id='materials' figure-id="tab:materials" figure-caption="Bill of materials">
    <s>[LEDs](https://www.adafruit.com/product/848) </s>                         <s>USD 10</s>
    <s>[LED HAT](https://tinyurl.com/ydh9wqp5) </s><s>USD 28.20 for 3 pieces</s>
    <s>[Power Cable](https://tinyurl.com/yaptpssu) </s><s>USD 7.80</s>
    <s>[20 Female-Female Jumper Wires (300mm)](https://www.adafruit.com/products/793) </s>         <s>USD 8</s>
    <s>[Male-Male Jumper Wire (150mm)](https://www.adafruit.com/products/1957)  </s>                         <s>USD 1.95</s>
    <s>[PWM/Servo HAT](https://tinyurl.com/yd8bdl2r) </s>                         <s>USD 17.50</s>
    <s>[Bumpers]() </s><s>TBD (custom made)</s>
    <s>[40 pin female header](https://www.adafruit.com/products/2222) </s>                   <s>USD 1.50</s>
    <s>[5 4 pin female header](http://www.digikey.com/product-detail/en/PPTC041LFBN-RC/S7002-ND/810144) </s><s>USD 0.60/piece</s>
    <s>[2 16 pin male header](http://www.digikey.com/product-detail/en/0022284160/WM50014-16-ND/313801) </s><s>USD 0.61/piece</s>
    <s>[12 pin male header](http://www.digikey.com/product-detail/en/amphenol-fci/68000-412HLF/609-3266-ND/1878525) </s><s>USD 0.48/piece</s>
    <s>[3 pin male header](http://www.digikey.com/product-detail/en/M20-9990345/952-2263-ND/3728227) </s><s>USD 0.10/piece</s>
    <s>[2 pin female shunt jumper](http://www.digikey.com/product-detail/en/382811-8/A26228-ND/293121) </s><s>USD 2/piece</s>
    <s>[5 200 Ohm resistors](https://tinyurl.com/yaramn3g) </s><s>USD 0.10/piece</s>
    <s>[10 130 Ohm resistors](https://tinyurl.com/y9vz2b9v) </s><s>USD 0.10/piece</s>
    <s>Total for `C0+wjd` configuration</s> <s>USD 212</s>
    <s>Total for `C1` components</s>                         <s>USD 77 + Bumpers</s>
    <s>Total for `C1` configuration</s>                         <s>USD 299+Bumpers</s>
 </col2>

</div>

TODO: add links to Bumpers: (a) bumper design files; (b) one-click purchasing option (?)

<style>
#materials {
    font-size: 80%;
}
#materials TD {
    text-align: left;
}
</style>

## LEDs

The Duckiebot is equipped with 5 RGB LEDs ([](#figure:led)). LEDs can be used to signal to other Duckiebots, or just make _fancy_ patterns.

The pack of LEDs linked in the table above holds 10 LEDs, enough for two Duckiebots.

<div figure-id="fig:led" figure-caption="The RGB LEDs">
     <img src="led.png" style='width: 15em'/>
</div>

### LED HAT

The LED HAT ([](#figure:led_hat)) provides an interface for our RGB LEDs and the computational stack. This board is a daughterboard for the Adafruit 16-Channel PWM/Servo HAT, and enables connection with additional gadgets such as [ADS1015 12 Bit 4 Channel ADC](https://www.adafruit.com/product/1083), [Monochrome 128x32 I2C OLED graphic display](https://www.adafruit.com/product/931), and [Adafruit 9-DOF IMU Breakout - L3GD20H+LSM303](https://www.adafruit.com/product/1714). This item will require [soldering](#soldering-boards-c1).

This board is custom degined and can only be ordered in minimum runs of 3 pieces. The price scales down quickly with quantity, and lead times may be significant, so it is better to buy these boards in bulk.

<div figure-id="fig:led_hat" figure-caption="The LED HAT">
     <img src="led_hat.png" style='width: 15em'/>
</div>

### PWM/Servo HAT

The PWM/Servo HAT ([](#figure:servo_hat)) mates to the LED HAT and provides the signals to control the LEDs, without taking computational resources away from the Rasperry Pi itself. This item will require [soldering](0_5_soldering_boards_c1.md).

<div figure-id="fig:servo_hat" figure-caption="The PWM-Servo HAT">
     <img src="servo_hat.png" style='width: 15em'/>
</div>

### Power Cable

To power the PWM/Servo HAT from the battery, we use a short (30cm) angled male USB-A to 5.5/2.1mm DC power jack cable ([](#figure:power-cable-usb-to-jack)).

<div figure-id="fig:power-cable-usb-to-jack" figure-caption="The 30cm angled USB to 5.5/2.1mm power jack cable.">
     <img src="power-cable-usb-to-jack.png" style='width: 15em'/>
</div>

### Male-Male Jumper Wires

The Duckiebot needs one male-male jumper wire ([](#figure:mm_wires)) to power the DC Stepper Motor HAT from the PWM/Servo HAT.

<div figure-id="fig:mm_wires" figure-caption="Premier Male-Male Jumper Wires">
     <img src="mm_wires.png" style='width: 15em'/>
</div>


### Female-Female Jumper Wires

20 Female-Female Jumper Wires ([](#figure:ff_wires)) are necessary to connect 5 LEDs to the LED HAT.

<div figure-id="fig:ff_wires" figure-caption="Premier Female-Female Jumper Wires">
     <img src="ff_wires.png" style='width: 15em'/>
</div>

## Bumpers

These bumpers are designed to keep the LEDs in place and are therefore used only in configuration `C1`. They are custom designed parts, so they must be produced and cannot be bought. We used laser cutting facilities. Our design files are available [here].

TODO: add links to .sldprt files once confirmed final version

<div figure-id="fig:bumpers" figure-caption="The Bumpers">
     <img src="placeholder.png" style='width: 15em'/>
</div>

## Headers, resistors and jumper

Upgrading `C0+wjd` to `C1` requires several electrical bits: 5 of 4 pin female header, 2 of 16 pin male headers, 1 of 12 pin male header, 1 of 3 pin male header, 1 of 2 pin female shunt jumper, 5 of 200 Ohm resistors and finally 10 of 130 Ohm resistors.

These items require [soldering](0_5_soldering_boards_c1.md).

<div figure-id="fig:headers" figure-caption="The Headers">
     <img src="placeholder.png" style='width: 15em'/>
</div>

<div figure-id="fig:resistors" figure-caption="The Resistors">
     <img src="placeholder.png" style='width: 15em'/>
</div>

TODO: Missing figures.
