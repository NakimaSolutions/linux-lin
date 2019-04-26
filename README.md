# LIN-bus at Czech Technical University

LIN (Local Interconnect Network) support and tools for Linux and SocketCAN.
<https://rtime.felk.cvut.cz/can/lin-bus/>

## slLIN - LIN Driver for Standard UART/TTY Interfaces

slLIN is TTY line discipline implemented for GNU/Linux operating system that
handles the interchange of LIN messages between the underlying UART driver and
the CAN bus subsystem.

This way, the same API as the one used for CAN networking can be used for
communication with LIN devices.

## Bibliography

* [Report describing proposal of LIN to SocketCAN integration](https://rtime.felk.cvut.cz/can/sllin-doc.pdf)
* [SocketCAN and UART Drivers Based LIN-bus Support for Linux](https://rtime.felk.cvut.cz/can/sllin-rtlws14-paper.pdf)
* [RTLWS14 paper](http://www.osadl.org/RTLWS-Submitted-Papers.rtlws14-submitted-papers.0.html)
