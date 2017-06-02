# I2C Device Spec

Address: 0x1C

Registers:

0x1A \(single byte storage\): write a byte to register 0x1A to save it \(an echo test would be writing a byte to 0x1A then immediately reading it back\)

0x20 \(sum byte 1 storage\): write a byte to store for the sum functionality \(**not implemented**\)

0x21 \(sum byte 2 storage\): write a byte to store for the sum functionality \(**not implemented**\)

0x2A \(sum result\): read 2 bytes from this register to see the sum of the bytes in 0x20 and 0x21 \(**not implemented**\)

0x3A \(one's complement\): write a byte here and the one's compliment will be stored \(**not implemented**\)



