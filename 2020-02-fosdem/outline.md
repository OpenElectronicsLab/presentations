% OpenElectronicsLab: Our Journey
% Ace Medlock, Kendrick Shaw, Eric Herman
% 2020-02-01

# Who we are
<!-- https://rmarkdown.rstudio.com/authoring_pandoc_markdown.html%23raw-tex#presentations -->
- Ace Medlock
- Kendrick Shaw
- Eric Herman

## in 2011, we didn't have these credentials
- Ace & Kendrick were graduate students

# ADS1290 breakout
 - through-hole with 1 64pin QFP
 - 2011-11-26 begin desgin
 - 2012-01-23 boards arrive
     - populated 2012 rev0 board
 - 2012-03-04 reading data

[https://github.com/OpenElectronicsLab/ads1298-breakout](https://github.com/OpenElectronicsLab/ads1298-breakout)

# ExG v0 Pix
![2012 board](../photos/eeg-mouse_rev_0.0-DSC00681.jpg)


# ExG Version 1
[https://github.com/OpenElectronicsLab/OpenHardwareExG](https://github.com/OpenElectronicsLab/OpenHardwareExG)
- 3 boards stacked, but testing of base-board hard
- example usage: [http://openelectronicslab.github.io/eeg-mouse/](http://openelectronicslab.github.io/eeg-mouse/)

# ExG Shield
[https://github.com/OpenElectronicsLab/OpenHardwareExG\_Shield](https://github.com/OpenElectronicsLab/OpenHardwareExG_Shield)
- designed testing, cheaper and easier for others
- made some errors and three different revs
- example usage: quantified self

# Holter Monitor
[https://github.com/OpenElectronicsLab/OpenHardwareHolterMonitor](https://github.com/OpenElectronicsLab/OpenHardwareHolterMonitor)
- asked for advice from Humatem and received some great guidance
- special purpose
- goal of certification
	- EC medical device regulation is currently changing (2020) and we don't really know the process yet
	- Need to design for safety from the start: Plan to do a ground-up redesign with eye on certification once we're happy with the prototype

# Many excellent FOSS tools to support hardware hackers
- for both hardware and firmware
- Arduino-type boards and tools lower the barrier to entry

# Arduino build environment
- Picture

# KiCAD
- schematic picture
- KICAD PCB
- Bare PCB
- Populated PCB

# OpenSCAD
- Picture

<!-- pass floor to Ace -->
<!--
Learn to Surface mount
hand solder, with one chip
youtube to learn
noise -> should go surface mount
let's just to SMD
Big board with solder paste
issues with solder paste, cold joints
Iron under the scope
- kinda ugly
- purpose is electrical connection, not pretty solder
Makes are still easy to make, but correctable
pix of green wire fixes and descriptions
learned a lot along the way
one of the things was safety
-->

# Surface mount is not something to be scared of
- great video examples on the net
- Do not fear the green wire fix, cutting traces
    - ![broken-pin-green-wire](../photos/kms15-shield-broken-pin-GreenwireZoomOut.jpg)
    - [fix PWRDWN and RESET: tie HIGH not LOW. D'oh!](https://github.com/OpenElectronicsLab/OpenHardwareExG_Shield/commit/507f61efbbbc3e7b2749c49335f21cd2c08a47c7)

# 0201 on the ActiveElectrode
- Picture

# testing
- big board was hard to test - getting a working board was hard; we now know
- we need to build testing into the design for bigger boards but we haven't mastered this skill yet. (Our current board is just smaller, and we didn't hand-solder it :) )
- Picture of testing harness for ExG\_Shield? Just a picture of big board?

<!-- end Ace -->

# Safety is important, and often fairly simple
<!--
https://en.wikipedia.org/wiki/Goggles#/media/File:Your_Quota_Two_eyes_that_see_Protect_them_2012_002_7217_xg94hq433_crop.tiff
(public domain from 1955 in USA, originally published without copyright notice)
-->
![goggles](../photos/Your_Quota_Two_eyes_that_see_Protect_them.png)


<!-- Ace hands floor to KMS -->

# General concepts
- What could go wrong?
- How serious is it
- How likely is it
- Risk = severity * probability
- Iterate design until risk is acceptable
  - freeclimbing
  <!-- moderate levels of risk more acceptable for yourself -->
  <!-- freeclimbing photo, not safe, but that can be an okay choice -->
  - Sometimes a high level of risk is acceptable
    - e.g. Defibrillator

# Risk of electrical shock
- Small currents can be dangerous when crossing the heart
- Current rather than voltage
    - Pacemaker voltages (~2 volts)
    - Minimum fibrilation currents
    - Resistances can be very low in a medical context
      - central lines, surgery, etc.
<!-- MAYBE Figure with patient and heart in circuit -->

# Isolation
- Batteries (Safety Extra Low Voltage, or SELV)
    - e.g.: unplugged laptop
- Creepage and clearance
  ![Creepage vs clearance](../photos/Creepage_vs_clearance.png)
- Power isolation
- Data isolation

# Leakage current standards

--------------------------------------------------------------------
Leakage Current    Body            Body Floating   Cardiac Floating
----------------- --------------- --------------- ------------------
Earth              500 $\mu$A      500 $\mu$A       500 $\mu$A

Enclosure          100 $\mu$A      100 $\mu$A       100 $\mu$A

Patient            100 $\mu$A      100 $\mu$A        10 $\mu$A
--------------------------------------------------------------------

- Can only be 2-5 times larger even if component fails
<!-- MAYBE Isolated, body float, cardiac float symbols -->

# Designing for failures
- Safe if any one component fails
- 2 means of patient protection
    - two layers of basic isolation
      vs. reinforced isolation
- Current limiting resistors on patient connections

# Take home message
- a little thought about safety goes a long way
- great tools and resources to support you
- don't be too intimidated
	- try
	- repeat
	- you'll improve as you go
- happy hardware hacking!

# References and Contacts

- Books and references
     - The Art of Electronics, Horowitz and Hill
     - Medical Instrumentation Aplication and Design, Webster
     - Texas Lude Man: https://www.youtube.com/watch?v=eg2hxpy--gg

- Contact
    - github
    - email addresses
