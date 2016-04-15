# PLC-Arduino
Project overview
Settimino is an open source Ethernet library for interfacing ARDUINO™ natively with
Siemens S7 PLCs. The CPUs 1200/1500 LOGO 0BA7 and S7200 are also supported.
Settimino is not strictly “the porting” of Snap7 for ARDUINO because, although it runs
fine in small boards such Raspberry™, its design (multiplatform 32/64 bit) is too
exacting for a tiny 8 bit board. I rewrote the Snap7 micro-client by optimizing its
footprint to be suitable with Arduino.
Main features
 Full PLC memory access.
 PDU independence, i.e. the data that you can transfer in a single call depends only
on the Arduino memory availability.
 Helper functions for data conversion (Big Endian --> Little endian)
 Three memory models for footprint optimization.
 Uses standard Arduino Ethernet library i.e. it can coexist with other clients/servers
in the same sketch.
 3 ms to read a PDU into the internal buffer, 24 ms for 1024 bytes into the external.
What do you need
To work with Settimino you need (see § Compatibility for details):
 An ARDUINO equipped with an Ethernet shield (with W5100) in which to load the
examples supplied.
 A Siemens PLC equipped with Ethernet port or Communication Processor.
Any PLC is supported except for the old S5 family.
Or, if you don’t have it, download Snap7 project (see below).
The Snap7 Library is not strictly required but I suggest you to download it (it’s free of
course) because it contains:
 A ready to run Client Demo (Win/Unix/BSD/Solaris) that allows you to see if what
you are transferring is correct without the needing of Simatic Manager.
 A ready to run Server Demo (same platforms) that emulates a S7300 PLC equipped
with Ethernet adapter that allows you to test your Settimino based
applications without having a physical PLC.
Even this documentation is derived from that of Snap7, visit its homepage for a more
detailed information.
See also § Testing Platforms.
