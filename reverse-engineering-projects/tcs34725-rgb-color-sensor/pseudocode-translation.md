DON'T FORGET TO \| 0x80 to REGISTERS



Needed: integration time, gain \(50ms, 4x in example code\)



Begin\(\) function



Start I2C

Read byte from ID register \(0x92\), we want back 0x44 or 0x10

Calls setIntegrationTime, setGain, and Enable

Set Integration time: write to register 0x81 value 0xEB

Set Gain: write to register 0x8F value 0x01

Enable:

* Write to register 0x80 value 0x01
* Wait 3 ms \(at least\)
* Write to register 0x80 value 0x03

Read from register 0x93, looking for 0x11 for valid setup



Getting the data:

Read 2 bytes from register 0x14 -- Clear Data

Read 2 Bytes from register 0x16 -- Red Data

Read 2 Bytes from register 0x18 -- Green Data

Read 2 Bytes from register 0x1A -- Blue Data

