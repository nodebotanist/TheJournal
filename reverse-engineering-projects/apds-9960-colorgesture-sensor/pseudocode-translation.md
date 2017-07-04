## Pseudocode Translation

Based on the [SparkFun Library](https://github.com/sparkfun/APDS-9960_RGB_and_Gesture_Sensor/)

#### The ADPS object contains properties for:

a delta for up-down and left-right gestures

a count for up-down, left-right, and near-far gestures

a gesture state

a `gesture_motion_` \(unknown purpose\)

#### Constructor

initializes the above properties

#### Destructor

No-op

#### Init function

Sets up an id variable

Begins I2C comms

Read ID register \(0x92\) and compare against known values for APDS-9960 \(0xAB or 0x9C\)

set enable register \(0x80\) to 0x00 \[disables all features, 0x7F to enable all\]

Set default ambient light and proximity registers:

* 0x81 to 219 \(ATIME\)
* 0x83 to 246 \(WTIME\)
* 0x8E to 0x87 \(PROX\_PPULSE\)
* 0x9D to 0 \(POFFSET\_UR\)
* 0x9E to 0 \(POFFSET\_DL\)
* 0x8D to 0x60 \(CONFIG1\)
* 


