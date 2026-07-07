
# DPDT Relay Working, Pinouts, Testing Explained
This document will cover how the DPDT relay actually works,
how we identify its pinouts.

DPDT relay stands for Double Pole Double Throw relay.
Double Pole means it has two independent switching contacts.
It contains eight pins in total, two for coil that moves the pole contacts
and six for switching external load with supply.

The project is a Relay Ring oscillator

## Testing The DPDT Relay with Meter
a simple way how we can check the pinouts of this relay using a multimeter.
First we can set the multimeter to continuity mode or resistance mode.

### Pin Orientation Confusion
Since there are many brands and types of DPDT relays,
the position of N/O and N/C pins can slightly differ from one brand to another.
Some relays have Common pin in the middle of each three-pin group and some have Common pin near the coil side.

So we should not depend only on online pictures or drawings,
but instead we should always verify using multimeter before connecting it into any circuit.

### Finding the Coil Pins
We can find the two coil pins by checking between every pair of pins.
Most two pins that show low resistance (normally between 200 to 500 ohms depending on relay coil voltage) are the coil terminals.

After that we can keep the coil unpowered and check among the remaining six pins.
We will find that in each group of three pins, one pin will show continuity with another pin,
that means these two are Common and N/C.

The third one will show no connection, that is N/O.
Now if we apply power to the coil then we will see that the continuity now shifts from N/C to N/O.

## How The DPDT Relay Works
Inside the relay, when the coil is not energized, the common pole pin stays connected to the N/C pin.
So that time the N/O pin remains open, but since the relay is an electromagnetic type device,
when we apply the rated voltage to the coil pins, then the coil becomes magnetized,
and it pulls the inner moving contact from the N/C side to the N/O side.

So we can say that before the coil gets power, the common stays with N/C.
When the coil gets power, then the common moves away from N/C and connects with N/O.

And when the coil power is removed again, then the inner contact goes back to its resting N/C position due to the spring force.
So it keeps toggling like that every time the coil is powered and de-powered.

## Sources
* [DPDT Relay Working, Pinouts, Testing Explained](https://www.homemade-circuits.com/dpdt-relay-working-pinouts-testing-explained/)
