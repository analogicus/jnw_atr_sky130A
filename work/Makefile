
#- Core makefile provides the following commands:
# -----------------------------------------------------------
# ip: generate ../design/<LIB> from ../cic/ip.json
# gds: generate gds/<CELL>.gds
# cdl: generate cdl/<CELL>.cdl
# lvs: Check cdl/<CELL>.cdl versus ../design/<LIB>/<CELL>.mag
# lpe: Extract parasitics lpe/<CELL>.spi
# drc: Run design rule checks on ../design/<LIB>/<CELL>.mag
# svg: Make schematic SVGs in ../documents/schematic.md
# -----------------------------------------------------------


PREFIX=JNWATR_
LIB=JNW_ATR_SKY130A
CELL=JNW_ATR

#- Which libraries to make SVG files for
SVGLIBS=JNW_ATR_SKY130A

#- Provide cells you want to check for the lvsall drcall commands
CELLS = JNW_ATR

include ../tech/make/core.make
