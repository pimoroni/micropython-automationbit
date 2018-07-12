# MicroPython automation:bit

MicroPython examples and documentation for the automation:bit

## automation:bit hardware

automation:bit has protected inputs, outputs, analog channels and a relay. These all map to existing pins on the micro:bit which you can just read/write as normal.

## Using automation:bit in MicroPython

### Outputs

automation:bit has two outputs:

* Output One - `microbit.pin14`
* Output Two - `microbit.pin15`

These are regular digital outputs, which you can toggle like so:

```python
microbit.pin14.write_digital(1)
```

### Inputs

automation:bit has two inputs:

* Input One - `microbit.pin8`
* Input Two - `microbit.pin13`

These act like regular digital inputs, although you should use them with an appropriate pull resistor since they're *very* sensitive. For example to read a button input you should include a 10k resistor pulling the input to 3v and the button bridging that to Ground.

```python
input_one_state = microbit.pin8.read_digital()
```

### Analog Inputs

automation:bit has three analog inputs, these consist of a protection circuit in front of the analog inputs on the micro:bit itself.

* Analog One - `microbit.pin2`
* Analog Two - `microbit.pin1`
* Analog Three - `microbit.pin0`

### Relay

automation:bit has a single relay connected to an output pin on the micro:bit;

* Relay One - `microbit.pin16`

### Variables

For convinience you might want to assign various automation:bit pins to variables, like so:

```python
import microbit

# automation:bit outputs 
output_one = microbit.pin14
output_two = microbit.pin15

# automation:bit inputs
input_one = microbit.pin8
input_two = microbit.pin13

# automation:bit analog
analog_one = microbit.pin2
analog_two = microbit.pin1
analog_three = microbit.pin0

relay = microbit.pin16
```
