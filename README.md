A circuit to use ESPhome as an IR blaster for an Olafus outdoor light.

I got these for crazy cheap on an Amazon deal.


<img width="1500" height="1423" alt="61VOVqrxBsL _AC_SL1500_" src="https://github.com/user-attachments/assets/136a344a-b232-4804-9a59-7d64122b3f2e" />

They're fine, but they're controlled by infrared only.  So I cloned the remote with a flipper zero and turned the commands into ESPhome code.  (Technically, Claude did)


It uses an N-channel mosfet to control the switching from the GPIO.

ESP32 5V (VIN) ── 47Ω ── IR LED 1 ── IR LED 2 ── 2N2222A collector


2N2222A emitter ── GND 


GPIO33 ── 1k ── 2N2222A base


<img width="2760" height="1800" alt="ir_led_driver_pictorial_v3" src="https://github.com/user-attachments/assets/a9965584-1730-486b-bd58-b4d240a4368b" />
