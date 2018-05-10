[top](README.md)

# Raspberry Pi CanaKit Assembly

What's in the CanaKit box?

<img src="images/canakit-contents-annotated.png" width="400"/>

The Raspberry Pi 3B+ comes with Ethernet and wireless adapters, three USB ports, and an HDMI port. That makes it a pretty good base for a general-purpose desktop computer.

The kit comes with most everything we need. Kits from other companies are similar. The micro-SD card is pre-loaded with New Out of Box Software, or NOOBS. That's a bootstrapper for installing an operating system. Without it, we'd have to build an operating system for the ARM architecture and load it onto a micro-SD ourselves. NOOBS is a time-saver.

The micro-SD adapter is included just in case we need to re-load the micro-SD card from a PC or Mac. 

Safety first: Put on your anti-static wristband. The photo shows a common ground point in the background. It's grounded to the building wiring, and connected to the anti-static mat and to the wristband.

<img src="images/anti-static.png" width="300"/>

One of the most challenging steps in assembling the unit is the removal of the paper backing from the self-adhesive heat sinks. Good luck.
<img src="images/heat-sinks-1.png | width=400

The larger heat sink goes on top of the Broadcom BCM2835 CPU. That's the relatively large square chip near the center of the board. The smaller heat sink goes on top of the SMSC LAN9514 USB Ethernet Controller. That's the smaller square chip located near the USB ports. Align the heat sinks carefully because they will stick up through openings in the case body.

<img src="images/heat-sinks-2.png" width="400"/>

The plastic case pulls apart into three parts like so:

<img src="images/case-disassembled.png" width="300"/>

The battery has nothing to do with the assembly. It's only there to lift one side of the case body for the photo.

Orient the board so that the micro-SD port aligns with the slot on the case bottom. 

<img src="images/case-bottom-align.png" width="300"/>

Gently insert the Pi into the case bottom. Slide the end opposite the USB ports under the plastic tabs at the corners of the base bottom and let the board lay down into the case bottom. Don't push on it; it doesn't snap in. 

<img src="images/placing-pi-in-case.png" width="300"/>

Slide the case body over the unit and onto the case bottom. They fit snugly together, but they don't snap. Be gentle. 

<img src="images/case-body-attached.png" width="300"/>

Fit the top of the case onto the body with the "leaves" of the Raspberry cut-out pointing toward the end where the USB ports are located. 

<img src="images/fully-assembled.png" width="300"/>

