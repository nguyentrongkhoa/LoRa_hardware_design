# **LoRa_prototype - Design Notes**

## **Overview**
<!-- Brief description of the PCB project -->

## **Schematic Notes**
<!-- Key circuit blocks, design rationale -->

## **Layout Considerations**
<!-- Layer stackup, impedance, keep-outs -->

# **Quectel L80-R GPS (U6)**

- Keep the module at least 5mm away from the nearest edge of the mother board, that is, it is better to  be placed in the   center of the mother board
- Patch antenna should point to the sky
- 30x30mm ground plane directly underneath the module
- Keep antenna at least 10mm away from tall metallic components
- Make sure the microcontroller, crystal, LCD, camera and other high speed components and
  interfaces are placed on the opposite side of the module
![Image](./images/imported_20260429_080856.png)

- Keep RF as far as away as possible
- Keep DCDC far away
- Enclosure should be non-metal around antenna, min distance 3mm
- Keep away from heat-generating circuits

M**CU (U10) and RF circuit**
- Keep RF traces short and straightforward to avoid reflections
- Place decoupling caps and RF parts first
- Do NOT** rou**te high-freq signals on board outline, since they will radiate
![Image](./images/imported_20260429_084340.png)

- Maintain 50-ohm characteristic impedance
- Avoid discontinuities (pad size too large for trace for example or inconsistent trace width)
![Image](./images/imported_20260429_084055.png)

- Avoid vias with RF signals
- RF return current paths must be free of obstacles (i.e no slots/cuts in the ground plane)
- Metal shield can be placed to reduce undesired radiation

![Image](./images/imported_20260429_084436.png)

- For STM32WL5x/Ex reference boards, GCPW (grounded coplanar waveguide)  is used as standard transmission line    structures
- Avoid thermal reliefs on RF lines, as they increase ESL
- Put vias around RF lines to reduce high-freq issues (via stitching)
![Image](./images/imported_20260429_083730.png)
---
- Power plane must NOT extend to board edge to avoid radiation 
- Ground planes must be put on all layers around the board outline and connected to each other (i.e no ground plane       should be left floating                                                                                                                                                           
![Image](./images/imported_20260429_085035.png)

RF Shielding:

- Good for passing EMC tests

- Can however cause parasitic capacitance or cavity resonances that can degrade signals to be protected

- Can act as a thermal trap

- Take care of critical RF traces and components first and then design shield, not the other 



---



Component Notes
**<**!**-- Click on designators like R1, C5, U3 to highlight on PCB -->**

**Power** **Distribution**
## **<!-- Power rails, decoupling strategy -->**

**Signa**l** Integrity**
## **<!-- Critical nets, routing constraints -->**

**Refer**e**nces**
## **<!-- D**a**tasheets, application notes, calculations -->**

---
KiNotes - PCBtools*.xyz*



