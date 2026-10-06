# µTari Go: A Handheld Atari 2600

![](https://raw.githubusercontent.com/nickbild/uTari_go/refs/heads/main/media/logo.png)

The **µTari Go** (pronounced micro-Tari) is a portable, handheld Atari 2600 built around my previous [**µTari**](https://github.com/nickbild/uTari) project. It plays original Atari 2600 cartridges using the original 6507 processor, TIA, and RIOT — no emulation and no FPGA.

My original µTari project shrunk the Atari 2600 motherboard from roughly 9.75 × 5.25 inches down to just 4.7 × 3.5 inches. I designed it with a future handheld version in mind, replacing the bulky switches and connectors with smaller alternatives and removing the RF modulator in favor of a composite video output.

µTari Go is that handheld. It combines the µTari board with a 4-inch CRT, built-in controls, speaker, audio amplifier, cartridge slot, and power circuitry inside a custom 3D-printed enclosure. It is a complete Atari 2600 that you can hold in your hands.

[Check out the YouTube video](https://www.youtube.com/watch?v=QAMx9kQR0u8)

*This project is an independent creation and is not affiliated with, endorsed by, or sponsored by Atari.*

## Real Atari Hardware

At its core are the same three chips responsible for running an original console:

- **6507** — CPU
- **TIA** — Television Interface Adapter responsible for graphics and audio
- **6532 RIOT** — RAM, I/O, and timer

![](https://raw.githubusercontent.com/nickbild/uTari_go/refs/heads/main/media/hardware_sm.jpg)

These chips are installed in my custom µTari PCB, which follows the original Atari 2600 circuit while eliminating hardware that isn't necessary for this application.

The original RF modulator is gone, for example. Instead, µTari produces composite video using a much simpler circuit consisting of a transistor and two resistors. The giant switches and full-size controller and cartridge connectors were also removed from the PCB.

## Adding a CRT

A real Atari deserves a CRT. µTari Go uses a **4-inch flat CRT display** mounted directly inside the enclosure. Composite video from the µTari connects to the display, so there isn't any digital video conversion between the Atari hardware and the screen.

Of course, putting a CRT into a handheld makes the device considerably larger than something built around a modern LCD, but it's worth it for me. The display technology is much closer to what an Atari 2600 would have originally been connected to.

## Controls

The front of the µTari Go has everything necessary to play games without an external controller.

Seven pushbuttons are used for the controls. Four sit underneath a 3D-printed D-pad, while the remaining three provide dedicated:

- **FIRE**
- **SELECT**
- **START**

The D-pad and buttons use separate 3D-printed switch carriers mounted behind the front panel.

The controls connect directly to the µTari hardware, so as far as the Atari is concerned, they behave just like the switches and joystick connected to a normal console.

This also explains one of the design decisions I made when creating the original µTari PCB. I replaced the normal Atari controller ports with pin headers specifically to make projects like this easier.

## Cartridge Slot

There wouldn't be much point in building a real Atari 2600 handheld if it couldn't accept real cartridges.

A **Sullins EBC12DRTH edge connector** provides the cartridge interface. It is mounted inside the case so cartridges can be inserted directly into the µTari Go.

![](https://raw.githubusercontent.com/nickbild/uTari_go/refs/heads/main/media/cartridge_port_sm.jpg)

## Audio

The Atari's audio output is fed into a **PAM8302 amplifier module**, which drives an **8-ohm speaker** mounted behind the grille in the back of the enclosure.

With the display, controls, cartridge connector, and speaker all built in, the µTari Go doesn't need any external hardware other than a power source and a game cartridge.

## Power

12V enters the console through a standard **2.1mm DC jack**. The CRT uses this 12V supply directly.

A **Pololu D45V5F9 step-down voltage regulator** provides a regulated 9V supply for the µTari. 

The power hardware is mounted inside the rear shell, with a 3D-printed clamp securing the DC jack in place.

## 3D-Printed Enclosure

Everything is packaged inside a custom [3D-printed case](https://github.com/nickbild/uTari_go/tree/main/models) consisting of front and rear shells along with the internal mounting hardware.

## Bill of Materials

- 1 x µTari
- 1 x 4-in flat CRT display
- 1 x PAM8302 audio amplifier module
- 1 x 8-ohm speaker
- 7 x pushbuttons
- 1 x Pololu D45V5F9 9V, 500mA Step-Down Voltage Regulator
- 1 x 2.1mm jack to screw terminal block
- 1 x Sullins EBC12DRTH edge connector
- 3D-printed case
- 8 x M2 6mm (D-pad and button switch carriers)
- 6 x M2 8mm (CRT retaining tabs)
- 4 x M2 10mm (2 for the DC jack clamp; 2 for the cartridge connector)
- 6 x M2 30mm (Joining the front and rear shells)

## Media

![](https://raw.githubusercontent.com/nickbild/uTari_go/refs/heads/main/media/console_off_sm.jpg)

![](https://raw.githubusercontent.com/nickbild/uTari_go/refs/heads/main/media/console_on_sm.jpg)

![](https://raw.githubusercontent.com/nickbild/uTari_go/refs/heads/main/media/console_on_close_sm.jpg)

![](https://raw.githubusercontent.com/nickbild/uTari_go/refs/heads/main/media/console_on_mid_sm.jpg)

## About the Author

[Nick A. Bild, MS](https://nickbild79.firebaseapp.com/#!/)

