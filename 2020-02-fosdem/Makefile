# $@ : target label
# $< : the first prerequisite after the colon
# $^ : all of the prerequisite files
# $* : wildcard matched part

VIEWER=evince
GENERATED_IMAGES=../photos/Creepage_vs_clearance.png ../photos/severity.png \
	../photos/openElectronicsLab_groupPhoto_small.jpg \
	../photos/eeg-mouse_rev_0.0-DSC00681_small.jpg \
	../photos/OpenHardwareExG-rev1-in-case.800_small.jpg \
	../photos/openhardware-exg-shield_small.jpg \
	../photos/populated-holtermonitor_small.jpg \
	../photos/REV0CHIP_small.jpg \
	../photos/youTubeSolderICs_small.jpg \
	../photos/surfaceMountTiny_small.jpg \
	../photos/solderPasteOnBoard_small.jpg \
	../photos/solderPasteMeltedMacro_small.jpg \
	../photos/solderPasteNotMelted_small.jpg \
	../photos/solderPasteJointHot_small.jpg \
	../photos/solderPasteJointCold_small.jpg \
	../photos/aceSolderingScope_small.jpg \
	../photos/handSolder01_small.jpg \
	../photos/handSolder02_small.jpg \
	../photos/handSolder03_small.jpg \
	../photos/handSolder04_small.jpg \
	../photos/handSolder05_small.jpg \
	../photos/handSolder06_small.jpg \
	../photos/handSolder07_small.jpg \
	../photos/handSolder08_small.jpg \
	../photos/handSolder09_small.jpg \
	../photos/uglyHandSolder_small.jpg \
	../photos/activeElectrodeC1micro_small.jpg \
	../photos/q10Wrong_unannotated_small.jpg \
	../photos/q10Wrong_annotated_small.jpg \
	../photos/rotatedPart_small.jpg \
	../photos/Q1-Q2_small.jpg \
	../photos/cutTrace_small.jpg \
	../photos/kms15-shield-broken-pin-GreenwireZoomOut_small.jpg \
	../photos/freeclimbing_small.jpg


default: pdf

pdf: clean outline.md $(GENERATED_IMAGES)
	pandoc --pdf-engine=xelatex outline.md -o outline.pdf -t beamer

%.png : %.svg
	inkscape --export-png $@ --export-dpi=300 $<

%_small.jpg : %.jpg
	convert $< -resize 1024 -quality 75 $@

check: pdf
	$(VIEWER) outline.pdf

clean:
	rm -vf outline.pdf $(GENERATED_IMAGES)
