# woodtrain electric locomotive

DIY Holz-Eisenbahn Elektrische Lokomotive

fun side project to build a electric locomotive that is compatible to [brio](https://www.brio.de/de-DE/produkte/eisenbahn/eisenbahnschienen-strassen) and [eichhorn](https://www.eichhorn-toys.de/eichhorn_en/categories/wooden-tracks-toy-trains/) wooden tracks.

## features

### main

-   as silent as possible
-   rechargeable
-   powerful - so it can track a long chain of wagons

### optional

-   self-select track-switch direction (kind of steering system)
-   remote control (optional)
-   smoke from chimney (_water vapor_)

## Ideas

### Power

18650 LiPoly Cell ([adafruit](https://www.adafruit.com/product/1781) ; [eckstein](https://eckstein-shop.de/PKNERGY-Lithium-Ion-Battery-ICR-18650-37V-2200mAh-LiPo-Li-Ion-with-JST-PH-Connector)

### Motor

first experiments will be with these mini stepper motors:

-   [2-phase 4-wire Mini 15mm Stepper Motor stepping 18 Degree with 12th Copper Gear](https://www.ebay.de/itm/404015504530)
-   [Mini 2-phase 4-Wire Stepper Motor 15MM Mini Stepping Motor 16teeth 0.25 Modulus](https://www.ebay.de/itm/404275426573)

### motor driver

based on [TCM2300 (Low voltage silent stepper motor driver)](https://www.analog.com/en/products/tmc2300.html)

hopefully i get to make a custom Featherwing with 2x TCM2300 onboard.
alternative we can use the [_breakout board_](https://www.reichelt.de/de/de/shop/produkt/breakout_board_fuer_tmc2300_schrittmotor-treiber-284703)

### controller

-   CircuitPython
-   ESP32-S3
-   Feather form factor

maybe one of these

-   [Adafruit ESP32-S3 Reverse TFT Feather - 4MB Flash, 2MB PSRAM, STEMMA QT](https://www.adafruit.com/product/5691)
-   [Adafruit ESP32-S3 Feather with STEMMA QT / Qwiic - 8MB Flash No PSRAM](https://www.adafruit.com/product/5323)
-   [FeatherS3 - ESP32-S3 Development Board by Unexpected Maker](https://www.adafruit.com/product/5399)

### wheel

3-layers of lasercut 0,8mm or 1mm birch plywood

traction with rubber band / o-ring
i will test these

-   [Präzisions O-Ring 24,00 x 2,00 mm NBR70 ](https://www.hug-technik.com/shop/Praezisions-O-Ring--24-00-x-2-00-mm--NBR70.html)
-   [Präzisions O-Ring 24,00 x 2,00 mm MVQ70 (Silikon)](https://www.hug-technik.com/shop/Praezisions-O-Ring-24-00-x-2-00-mm-MVQ70.html)
-   [Präzisions O-Ring 24,00 x 2,50 mm NBR70](https://www.hug-technik.com/shop/Praezisions-O-Ring--24-00-x-2-50-mm--NBR70.html)
-   [Präzisions O-Ring 24,00 x 2,50 mm MVQ70 (Silikon)](https://www.hug-technik.com/shop/Praezisions-O-Ring-24-00-x-2-50-mm-MVQ70.html)

## case

laser cut birch plywood
TbD

## Information

### track gauge (Spurbreite):

| manufacture | min  | max  | width | target |
| ----------- | ---- | ---- | ----- | ------ |
| BRIO        | 19mm | 30mm | 5,5mm | 24,5mm |
| Eichhorn    | 20mm | 32mm | 6mm   | 26mm   |
| minimal     | 20mm | 30mm | 5mm   | 25mm   |
|             |      |      |       |        |

### wheel Ø

Normal wheel is Ø ~20mm

as this has difficulties when the joints between track segments leave some space
we try with bigger wheel Ø.

### design targets

-   25mm track gauge
-   \>= 24mm Ø wheel

## random things

## state

ToDo-List

-   find FeatherWing template for kicad
    -   https://gitlab.com/kicad/libraries/kicad-templates/-/tree/master/Projects?ref_type=heads
    -   https://github.com/whmountains/FeatherWing-template-KiCad
    -   https://github.com/mignon-p/FeatherWing-template-KiCad/tree/master/FeatherWing_KC5
-   create dual TMC2300 FeatherWing
    -   https://shop.watterott.com/SilentStepStick-Protector-Schutz-fuer-Schrittmotortreiber
    -   https://github.com/watterott/SilentStepStick/blob/master/hardware/StepStick-Protector_v20.pdf
-   write CircuitPython TMC2300 library
    -   https://github.com/analogdevicesinc/PyTrinamic/issues/118
    -   https://github.com/analogdevicesinc/PyTrinamic/blob/master/pytrinamic/ic/TMC2300.py
    -   https://github.com/teemuatlut/TMCStepper
    -   https://forum.arduino.cc/t/arduino-and-tmc2300/873439

# License

<!-- license info -->
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/">
    <img alt="Creative Commons License" style="border-width:0"
        src="https://i.creativecommons.org/l/by/4.0/88x31.png" />
</a>
<br />
<span xmlns:dct="http://purl.org/dc/terms/" property="dct:title">
    all files in woodtrain-locomotive
</span> by
<a xmlns:cc="http://creativecommons.org/ns#"
        href="https://github.com/s-light/VARTA_Powerpack_Type_57959"
        property="cc:attributionName"
        rel="cc:attributionURL">
    Stefan Krüger (s-light)
</a>
are licensed under a<br/>
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/">
    Creative Commons Attribution 4.0 International License
</a>.

all software parts/files are licensed under [MIT](LICENSE).

i see this project as [Open Source Hardware (OSHW)](https://www.oshwa.org/definition/)

![OSHW logo](http://www.oshwa.org/wp-content/uploads/2014/03/oshw-logo.svg)

<!-- license info end -->
