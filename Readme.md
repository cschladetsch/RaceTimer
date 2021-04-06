# Race Timer

Time from when RC car moves to when (same) car returns. 

* Target is Arduino, with a view to using Pi.
* Only one car on circuit at a time.

* Add obstacles for lap.

* Target is drift cars.

* Add Lap Time, Slowest and Fastest Lap times.

Have fun with friends trying to get fastest time using drifting on Veterra Nissan GT3!

There are limits to the proximity sensor, and there should be a way to differentiate cars.

Maybe Bluetooth app for phones?

## Problems

* Make sure car slows down to < 10m/s to record an 'end'
  * Sensor has about 25/s sampling time, up to 400cm. Would have to be reduced to 200cm at most.
  * That means a length of 36cm could be missed. Many cars are shorter than this.
    * Mine is about 38cm.
    * Either increase poll frequency (not possible cheaply), or
    * Make cars longer. Not possible, or
    * Make cars have to travel slower to register with sensor (ding ding ding!)
      * This could actually be cool: force drivers to slow down to register end of race
      * Takes skill to reach to optimal slowest speed
* How to distinguish cars?
  * Use Printed QR codes to recognise cars
    * Requires more sensors on unit, and lots of extra code
    * How to print the QR codes?
    * Have a label maker - would that be useful?
  * \>>> name <<<
    * Use `dlib` to recognise given markers like <<< and >>> and start and end
    * Could work on Arduino but not Pi
    * Can be printed on a label-maker on field
    * Error prone
  * Electronically?
    * Add a Pi to each car (not ideal)
    * This would solve a lot of problems.
    * No visual pattern recognition needed.



