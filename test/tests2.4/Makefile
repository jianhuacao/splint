.PHONY: emptycase enumtest duffs bitfields bugs tests hexconstants innercomment nothing offsetof komazi print syslog error ulrich cpptest longlong subdir fink driverstub alignof source emptycase enumtest duffs bitfields bugs tests hexconstants innercomment nothing offsetof komazi print syslog error ulrich cpptest longlong subdir fink driverstub alignof source

SPLINT = splint

all: check

check: emptycase enumtest duffs bitfields bugs tests hexconstants innercomment nothing offsetof komazi print syslog error ulrich cpptest longlong subdir fink driverstub alignof source 

emptycase:
	$(SPLINT) emptycase.c 

enumtest:
	$(SPLINT) enumtest.c -expect 2

duffs:
	$(SPLINT) duffs.c -expect 7

bitfields:
	$(SPLINT) bitfields.c

bugs:
	$(SPLINT) bug1.c 
	$(SPLINT) bug2.c -expect 5 
	$(SPLINT) bug3.c -expect 3

tests:
	$(SPLINT) test0.c 
	$(SPLINT) test1.c 
	$(SPLINT) test2.c 

hexconstants:
	$(SPLINT) hexconstants.c -expect 1 
	$(SPLINT) +checks hexconstants.c -expect 4

innercomment:
	$(SPLINT) innercomment.c -expect 2 +forcehints 
	$(SPLINT) innercomment.c -nestcomment

nothing:
	$(SPLINT) nothing.c 

offsetof:
	$(SPLINT) offsetof.c -expect 2 

komazi:
	$(SPLINT) komazi.c 

print:
	$(SPLINT) print.c 

syslog:
	$(SPLINT) syslog.c +unixlib 

error:
	$(SPLINT) error.c -expect 1 

ulrich:
	$(SPLINT) ulrich.c -expect 1

cpptest:
	$(SPLINT) cpptest.c '-D__P(x)=x' -expect 1

longlong:
	$(SPLINT) longlong.c -expect 4

subdir:
	$(SPLINT) subdir/main.c subdir/main.lcl

fink:
	$(SPLINT) fink.c 

driverstub:
	$(SPLINT) driverstub.c -sysdirs "/usr/"

alignof:
	$(SPLINT) alignof.c -expect 2

source:
	$(SPLINT) -D DBL_MANT_DIG=25 source.c -expect 1









