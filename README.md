# SOLO12_head

## Features
Quantity|Reference|Voltage|Intensity|Resistance|Detail
---|---|---|---|---|---|
1|SLS X-Cube 850mAh lithium polymer batteries|24V(2x3S)|30C continous = 2 x 30 x 0.85 = 51A 60C burst = 2 x 60 x 0.85 = 102A |/|[More informations of SOLO batteries](https://github.com/open-dynamic-robot-initiative/open_robot_actuator_hardware/blob/master/mechanics/quadruped_robot_12dof_v1.1/README.md#off-the-shelf-components)|
1|[uDriverv2](https://github.com/open-dynamic-robot-initiative/open_robot_actuator_hardware/tree/master/electronics/micro_driver_electronics)|
2|[IPower GM2804 (+ AS5048A encoder)](https://www.robotshop.com/ca/fr/moteur-cardan-ipower-gm2804-avec-encodeur-as5048a.html)|10V|0.07-5A|5.57Ω|Hollow shaft diameter|5.7mm ([IPower GM2804 Drawings](https://user-images.githubusercontent.com/103576080/168556596-d6f692c8-2cbd-48c1-b92e-5072b6c10471.jpg))|
2|[AEDB-9140-A13 optical encoder](https://fr.rs-online.com/web/p/codeurs/7967806)|
2|[I2S MEMS (MicroElectroMechanical Systems) microphone for Raspberry Pi]()|
1|[Arducam OG02B10 2MP Global Shutter color camera module](https://www.robotshop.com/eu/fr/module-camera-couleur-arducam-2mp-global-shutter-og02b10-pivariety.html)|
1 | Raspberry Pi CM4|5V|3A|

## Minimum power wires section
Raspberry Pi 4 intensity max + Motor intensity max = 8A

S = (ρ x 2L x I)/U’ = 0.021 x 2 x 8 / (24 x 0.3) = 0.46mm²

S = (ρ x 2L x I)/U’ = 0.021 x 2 x 8 / (48 x 0.3) = 0.23mm²

Unit | Detail |
--- | --- |
ρ | coper resistance = 0.021|
L | cable length (go+back)|
I | system intensity|
U' | voltage drop = system voltage x 3%|

So, for a 24V battery voltage, a battery intensity max of 8A and a 1m cable length (2m in the up table) a 0.5mm² cable section be sufficient. Usualy 0.5mm² section cable have ~Ø2.6mm outer diameter. For information, currently 1mm² section are used on SOLO quadruped robot to power legs uDriverv2.

## Raspberry Pi communication wires
![ethernet_connector](https://user-images.githubusercontent.com/103576080/168591434-17662cf1-bd75-4484-a176-0e60005cda20.png)
Self-made ethernet wire with 4 connections
![connection_wire_2](https://user-images.githubusercontent.com/103576080/168591920-0208964b-89a3-48ea-95b0-03c5cc778b7f.jpg)
Robot interface wire
![Screenshot 2022-05-16 at 14-37-03 open_robot_actuator_hardware_details_components md at master · open-dynamic-robot-initiative_open_robot_actuator_hardware](https://user-images.githubusercontent.com/103576080/168593933-6c000e5b-0e00-470e-8276-c44ba41003b3.png)
4 Ethernet wires RS 180-6028 (0.14mm²/~Ø1.5mm)

[More information](https://github.com/open-dynamic-robot-initiative/open_robot_actuator_hardware/blob/master/electronics/details/details_wiring.md#robot-interface-wire)

## SOLO head wire
Hollow shaft superficy : π(5.7/2)² = 25.52mm²

Wire superficy : 2π(2.6/2)² + 4π(1.5/2)² = 17.69mm²

17.69mm² < 33.18mm² => OK
