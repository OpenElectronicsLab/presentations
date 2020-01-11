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
