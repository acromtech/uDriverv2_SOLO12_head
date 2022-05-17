# SOLO12_head

## Features
Quantity|Reference|Voltage [V]|Intensity [A]|Detail
---|---|---|---|---|
1|[SLS X-Cube 850mAh lithium polymer batteries](https://github.com/open-dynamic-robot-initiative/open_robot_actuator_hardware/blob/master/mechanics/quadruped_robot_12dof_v1.1/README.md#off-the-shelf-components)|24(2x3S)|30C continous = 2 x 30 x 0.85 = 51<br>60C burst = 2 x 60 x 0.85 = 102 |/|
1|[uDriverv2](https://github.com/open-dynamic-robot-initiative/open_robot_actuator_hardware/tree/master/electronics/micro_driver_electronics)|5-32|/|/|
2|[IPower GM2804 (+ AS5048A encoder)](https://www.robotshop.com/ca/fr/moteur-cardan-ipower-gm2804-avec-encodeur-as5048a.html)|10|0.07-5|Hollow shaft diameter : 5.7mm <br> [Drawings](https://user-images.githubusercontent.com/103576080/168556596-d6f692c8-2cbd-48c1-b92e-5072b6c10471.jpg) <br> Resistance : 5.57Ω|
2|[AEDB-9140-A13 optical encoder](https://fr.rs-online.com/web/p/codeurs/7967806)|(-0.5)-7|0.001-0.018|/|
2|[I2S MEMS (MicroElectroMechanical Systems) microphone for Raspberry Pi](https://makersportal.com/shop/i2s-mems-microphone-for-raspberry-pi-inmp441)|/|/|/|
1|[Arducam OG02B10 2MP Global Shutter color camera module](https://www.arducam.com/product/arducam-2mp-og02b10-global-shutter-color-camera-modules-for-raspberry-pi/)|/|/|/|
1 | Raspberry Pi CM4|5|3|/|

## Minimum power wires section
Raspberry Pi 4 maximum intensity + Motor maximum intensity = 8A

>S = (ρ x 2L x I)/U’ = 0.021 x 2 x 8 / (24 x 0.3) = 0.46mm²<br>S = (ρ x 2L x I)/U’ = 0.021 x 2 x 8 / (48 x 0.3) = 0.23mm²

Unit | Detail |
--- | --- |
ρ | coper resistance = 0.021|
L | cable length (go+back)|
I | system intensity|
U' | voltage drop = system voltage x 3%|

So, for a 24V battery voltage, a battery intensity max of 8A and a 1m cable length (2m in the up table) a 0.5mm² cable section be sufficient. Usualy 0.5mm² section cable have ~Ø2.6mm outer diameter. 
>Currently 1mm² section are used on SOLO quadruped robot to power legs uDriverv2.

## Raspberry Pi communication wires
Self-made ethernet wire with 4 connections|Robot interface wire|
---|---|
![ethernet_connector](https://user-images.githubusercontent.com/103576080/168591434-17662cf1-bd75-4484-a176-0e60005cda20.png) | ![connection_wire_2](https://user-images.githubusercontent.com/103576080/168591920-0208964b-89a3-48ea-95b0-03c5cc778b7f.jpg)
> Four RS 180-6028 wires (0.14mm²/~Ø1.5mm) are fixed to the ethernet connector ([more informations](https://github.com/open-dynamic-robot-initiative/open_robot_actuator_hardware/blob/master/electronics/details/details_wiring.md#robot-interface-wire))

## SOLO head wire
>Hollow shaft superficy : π(5.7/2)² = 25.52mm² <br> Wire superficy : 2π(2.6/2)² + 4π(1.5/2)² = 17.69mm²

17.69mm² < 25.52mm² => OK
