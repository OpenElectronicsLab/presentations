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

# ExG Version 0
 - through-hole with 1 64pin QFP
 - 2011-11-26 begin desgin
 - 2012-01-23 boards arrive
     - ![2012 board](../photos/eeg-mouse_rev_0.0-DSC00681.jpg)
     - populated 2012 rev0 board
 - 2012-03-04 reading data

# ExG Version 1
- 3 boards stacked, but testing of base-board hard
- example usage: eeg-mouse

# ExG Shield
- designed testing, cheaper and easier for others
- made some errors and three different revs

# Holter Monitor
- special purpose
- goal of certification


# Arduino build environment
- Picture

# lower barriers, FOSS tools are great
- Arduino-type boards lower the barrier to entry

# KiCAD
- schematic picture
- KICAD PCB
- Bare PCB
- Populated PCB

# OpenSCAD
- Picture

# Learning surface mount soldering
![2012 board](../photos/REV0CHIP)
*rev0: through-hole except the chip*
<!-- our first board was through-hole soldered, except the chip. -->

# Learning surface mount soldering
- "Pin sweep" method of soldering ICs
- I learned it by watching YouTube!
![YouTube](../photos/youTubeSolderICs.jpg)
<!-- At first we were intimidated by the tiny feet, but after watching some YouTube videos we were willing to give it a try - and it worked!
We felt like our first board had too much noise for what we wanted to do, so in our second design we focused on reducing noise - and that meant making the leap to all surface-mount components. -->

# Learning surface mount soldering
![surface mount 0603](../photos/surfaceMountTiny)
*0603 surface mount resistor*
<!-- surface mount components are tiny -->

# Solder paste
![solder paste](../photos/solderPasteOnBoard)
*solder paste applied to a board*
<!-- so we thought it would be good to use solder paste a hot air gun. You apply the solder paste using a stencil, you end up with sticky paste just on the pads, and then you stick your component into the paste and heat it up with a hot air gun. Easy! -->

# Solder paste
![solder paste melted](../photos/solderPasteMeltedMacro)
*surface mount components soldered with solder paste*
<!-- After you apply the hot air gun, you get something like this, which looks fine... Except when we tested the board, it didn't work. We seemed to have a lot of bad solder joints. In trying to find the bad joints, I took the board under the microscope, and then I figured out why... -->

# Solder paste
![solder 10x](../photos/solderPasteNotMelted)
*Solder paste under the microscope*
<!-- This is what solder paste looks like under the microscope. It's actually a bunch of little beads of solder, held together by paste. -->

# Solder paste
![solder paste joint OK](../photos/solderPasteJointHot)
*solder paste joint: OK*
<!-- Some joints look like this - these are OK. -->

# Solder paste
![solder paste joint cold](../photos/solderPasteJointCold)
*solder paste joint: cold solder*
<!-- But some look like this. Does this conduct electricity? Maybe. Probably not reliably. I found it really hard to tell which joints were OK. So, new plan: -->

# Soldering using a dissection scope
![soldering under scope](../photos/aceSolderingScope)
*using a microscope for soldering*
<!-- Use a microscope and hand-solder -->

# Hand-soldering surface mount
- The job of a solder joint is to conduct electricity, not to look pretty
![solder joint ugly](../photos/uglyHandSolder)
*ugly, but works*
<!-- Using this method does not result in pretty solder joints. But the job of a solder joint is to conduct electricity, not to look pretty. -->

# Hand-soldering surface mount
![hand-soldered 0201](../photos/activeElectrodeC1micro)
*hand-soldered 0201 capacitor*
<!-- You can even do an 0201 package - I refer to these as breathably small components. -->

# Fixing misteaks
- You will make mistakes. You will be able to fix them.
![rotated part](../photos/rotatedPart)
*rotated Q*
<!-- One thing a hot air gun is good for is fixing mistakes. And you will make mistakes. That's OK, you'll also fix them. In this case, we used the wrong footprint for the component that we chose. The pads are G-S-D, while the feet are D-G-S. So we just picked it up, rotated it, and stuck it back down. -->

# Fixing mistakes
![rotated Q1-Q2](../photos/Q1-Q2)
*flipped Q1-Q2*
<!-- But that wasn't the worst error on this board - Q1-Q2 had pin 1 and 2 reversed. This was my solution - turn the component 180 degrees and greenwire pin 3 to its pad. We also needed to add a couple resistors that we forgot. -->

# Fixing mistakes
![cut traces](../photos/cutTrace)
*cut traces*
<!-- So what if you put a trace where you shouldn't have one? Well, you can just get a razor blade and cut it... provided you have a two-layer board. Or you can try lifting the foot of the IC up off the pad... -->

# Fixing mistakes
![broken-pin-green-wire](../photos/kms15-shield-broken-pin-GreenwireZoomOut.jpg)
*green wire into the chip*
<!-- And if you accidentally break off the foot while doing that... then you can just dremel into the chip itself, and hook the wire up straight to the chip. This is Kendrick's work, by the way. The problem was that PWRDWN and RESET should have been tied HIGH not LOW. D'oh! (https://github.com/OpenElectronicsLab/OpenHardwareExG_Shield/commit/507f61efbbbc3e7b2749c49335f21cd2c08a47c7)
-->



<!-- May or may not mention Testing:
# testing
- big board was hard to test - getting a working board was hard; we now know 
- we need to build testing into the design for bigger boards but we haven't mastered this skill yet. (Our current board is just smaller, and we didn't hand-solder it :) )
- Picture of testing harness for ExG_Shield? Just a picture of big board?
-->

# Safety is important, and not that hard!

# General concepts
- What could go wrong?
- How serious is it
- How likely is it
- Risk = severity * probability
- Iterate design until risk is acceptable

# Sometimes a high level of risk is acceptable
  - Stock mad science photo
  - e.g. Defibrillator

# Leakage currents
- Crossing the heart
- Current rather than voltage
    - Pacemaker voltages (~2 volts)
    - Minimum fibrilation currents
- Figure with patient and heart in circuit

# More risks in medical environment
 - Stock photo (central line X-ray?)
 - unconscious/disabled patients (unable to withdraw)
 - spills/injuries
 - central lines

# Leakage current standards
- Table
- Isolated, body float, cardiac float symbols

# Isolation
- Batteries (SELV)
    - e.g.: unplugged laptop
- Power isolation
- Data isolation
- Creepage and clearance

# Designing for failures
- 2 means of patient protection
    - two layers of basic isolation
      vs. reinforced isolation
- Safe if any one component fails
- Protection resistors

# certification (ongoing)
- EC medical device regulation is currently changing (2020) and we don't really know the process yet
- Need to design for safety from the start: Plan to do a ground-up redesign with eye on certification once we're happy with the prototype

# References and Contacts

- Books and references
     - The Art of Electronics, Horowitz and Hill
     - Medical Instrumentation Aplication and Design, Webster
     - Texas Lude Man: https://www.youtube.com/watch?v=eg2hxpy--gg

- Contact
    - github
    - email addresses
