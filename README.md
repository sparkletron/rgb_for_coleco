# RGB for Colecovision
### Schematic and PCB for production of a sub rf replacement board that is Genesis 9 pin compatible.

---

  author: Jay Convertino

  date: 2023.07.10

  details: Converts internal YPbPr to RGB to Pound Genesis cable (Genesis compatible outputs)

  license: MIT

---

## LICENSE
  - All files related to or generated from the KiCAD source fall under the MIT license.
  - All files generated by me, Jay Convertino, fall under the MIT license.
  - All files from other sources fall under the license of their specification.

## RELEASE VERSIONS
### Current
  - 0.5 BETA

### Past
  - DEV

## Intro

  This circuit is a replacment for the sub rf board of the original colecovison.

## SOURCES
### RGB conversion
  - TMS RGB : https://tms-rgb.com/ : Nicholas Piegdon

  Special thanks to Nicholas Piegdon. For using the TI YPbPr chip in his design and coming up with the resistor values to obtain proper color
  balance from a TMS9928. This circuit uses a different method for the too much blue. In this case it switches to a sample generated internally by the coleco that is also used to set the DC offset during sync. Also the driver is based on being compatible with the sega
  genesis. This works well with the Pound cable, yes its kinda crap, but its cheap and provides a baseline from which you can only go up.

## REQUIREMENTS
  - KiCAD v7.X

## BUILD TIPS
  This design is made so anyone can build this. You may send it out to a fab house, you may use a PCB mill, or even etch it.
  This is possible since the components can serve as the plated through hole. Other holes can simply have a solid piece of
  wire inserted and soldered to complete the connection (excess resistor leads is a great option).

  Recommend removing the Y, Pb, Pr inductors that are inline if they are there. They will cause color smearing.

  Output composite resistors and cap are optional, can replace the resistor connecting the output to the inverting input with a jumper.
  If no gain is wanted.
