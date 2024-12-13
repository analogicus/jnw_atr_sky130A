
all:
	${foreach c, ${CELLS}, ${MAKE} run NAME=${c};}


include ../tech/make/sim.make

include ../cic/cells

LIB=JNW_ATR_SKY130NM
CELL=JNW_ATR
PREFIX=JNWATR_

TCELL=PCH_4C1F2

test:
	${MAKE} run CORNER="typical" NAME=${TCELL}
	#test -f ${PREFIX}${TCELL}/output_dc/dc_SchGtKttTtVt.yaml || exit;
	#cat ${PREFIX}${TCELL}/output_dc/dc_SchGtKttTtVt.yaml |grep gmid10_vgs|perl -ne '($$k,$$v) = split(/ /);if($$v < -1){exit 0;}{exit 1;}'

post:
	${foreach c, ${CELLS}, cat header.md ${PREFIX}${c}/README.md > ../docs/_mos/${PREFIX}${c}.md;}

run:
	test -d ${PREFIX}${NAME} && cd ${PREFIX}${NAME} && make ${CORNER} OPT=${OPT}

gen:
	python3 gendirs.py

parse:
	python3 parse.py

summary:
	python3 plot.py
	cat header.md README.md > ../documents/all.md
