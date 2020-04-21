# Section 3: AMPLIFIERS
## 3.1 Operational Amplifier(Op-amp)
### 3.1.1 Introduction
An operational amplifier is basically a high gain,direct coupled amplifier. It has two inputs 
and an one output, but generally it is operated in single ended input-single ended
output mode. The differential amplifier forms the first stage of an op-amp. Opamp can
perform several arithmetic operations like addition, subtraction, differentiation, integration,
comparison, analog to digital conversion etc. Opamp are used is analog computers.

<p align="center">
<img src="https://user-images.githubusercontent.com/63674480/79279637-15a84980-7ecc-11ea-9c91-2d6b1359765b.png"/>
</p>
                                              
                                          Figure 3.1: schematic symbol of Op-amp

                              
IC 741 is widely used Op-amp. In this IC when input is zero, the output can be adjusted
to zero by varying the 10K potentiometer between offset null terminal.

### 3.1.2 Virtual Ground and Summing Point Constraint

**Valid only when the OA is under negative feedback**

Due to the large open loop gain of the OA, the difference between the voltages at the inverting and
non-inverting terminals is vanishingly small. Thus, if the non-inverting terminal is grounded (i.e. Real Ground,
), then the inverting terminal is also assumed to be at ground potential , even though actually it may
not be so. This terminal is Known as Virtual Ground (to distinguish it from actual ground).

The assumption that V<sup>+</sup>=V<sup>-</sup> as well as i<sub>1</sub>=i<sub>2</sub> is known as the 
Summing Point Constraint. These two assumptions make the analysis of OA circuits absolutely trivial
Extending this argument, we can say that for OAs under negative feedback, the voltages at the inverting
and non-inverting terminals always track each other, such that their difference is zero (almost!)

**Caution:-** These assumptions are applicable only for OAs under negative feedback, never apply these
assumptions when the OA is under positive feedback.

### 3.1.3 Negative Feedback:

Here the output of the Op-Amp is connected to its Inverting ( – ) input, thus the output is fed back to the input so as to reach an equilibrium. Thus the input signal at the Non Inverting (+) input will be reflected at the output. The Op-amp with the negative feedback will drive its output to level necessary and hence the voltage difference between its inverting and non inverting inputs will be almost zero.

### 3.1.4 Positive Feedback

Here the output voltage is fed back to the Non inverting (+) input. The input signal is fed to the Inverting input. In positive feedback design, if the Inverting input is connected to ground, then the output voltage from the Op-amp will depends on the magnitude and polarity of voltage at the Non inverting input. When the input voltage is positive, then the output of the Op-Amp will be positive and this positive voltage will be fed to the Non inverting input resulting in a full positive output. If the input voltage is negative, then the condition will be reversed.


### 3.1.5 Block diagram and inputs

<p align="center">
<img src="https://user-images.githubusercontent.com/63674480/79919797-ae027900-844c-11ea-967f-429f34877b23.png"/>
</p>         

                                           Figure 3.2: Block diagram of Opamp

An opamp has two input terminals:
1. Non-inverting input: output signal is in phase with input signal, denoted by (+).
2. Inverting input: output signal is out of phase with input signal, denoted by (-).
 
### 3.1.6 Inverting Opamp

In this configuration, the output is fed back to the negative or inverting input through a resistor (R2). The input signal is applied to this inverting pin through a resistor (R1).

The positive pin is connected to ground.

<p align="center">
<img src="https://user-images.githubusercontent.com/63674480/79920585-0f771780-844e-11ea-942c-614a4e5a1fb4.png"/>
</p>

                                            Figure 3.3: Inverting Opamp

<p align="center">
<img src="https://user-images.githubusercontent.com/63674480/79920635-287fc880-844e-11ea-893c-0efeb1eb7a4e.png"/>
</p>

This is evident in the special case where R1 and R2 are equal. This configuration allows for the production of a signal that is complementary to the input, as the output is exactly the opposite of the input signal.

Due to the negative sign, the output and input signals are out of phase. If both signals must be in phase, a non-inverting amplifier is used.

### 3.1.7 Non-inverting Opamp

This configuration is very similar to the inverting operation amplifier. For the non-inverting one, the input voltage is directly to the applied to the non-inverting pin and the end of feedback loop is connected to ground.

<p align="center">
<img src="https://user-images.githubusercontent.com/63674480/79920684-4816f100-844e-11ea-82d5-5426bc613aa5.png"/>
</p>

                                            Figure 3.4: Non-inverting Opamp


<p align="center">
<img src="https://user-images.githubusercontent.com/63674480/79920740-67158300-844e-11ea-88e9-9dc5d880d60a.png"/>
</p>

These configurations allow amplification of one signal. It’s possible to amplify several signals by using summing amplifiers.

### 3.1.8 Non-inverting Summing Amplifier

To add 2 voltages, only 2 resistors can be added on the positive pin to the non-inverting operational amplifier circuit.

<p align="center">
<img src="https://user-images.githubusercontent.com/63674480/79921452-d770d400-844f-11ea-906f-3421748a0395.png"/>
</p>

                                             Figure 3.5: Non-Inverting Summing Amplifier
                                             

<p align="center">
<img src="https://user-images.githubusercontent.com/63674480/79921529-f53e3900-844f-11ea-8cbe-07421c30614b.png"/>
</p>

It is worth noticing that adding several voltages is not a very flexible solution. Indeed, if a 3<sup>rd</sup> voltage is added with exactly the same resistances, the formula would be Vs = 2/3 (V<sub>1</sub> + V<sub>2</sub> + V<sub>3</sub>).

The resistors would need to be changed to get Vs = V<sub>1</sub> + V<sub>2</sub> + V<sub>3</sub>, or a 2<sup>nd</sup> option is to use an inverting summer amplifier.

### 3.1.8 Inverting Summing Amplifier

By adding resistors in parallel on the inverting input pin of the inverting operation amplifier circuit, all the voltages are summed.

<p align="center">
<img src="https://user-images.githubusercontent.com/63674480/79921752-87ded800-8450-11ea-89b7-f119d5993e76.png"/>
</p>

                                             Figure 3.6: Inverting Summing Amplifier
                                             

<p align="center">
<img src="https://user-images.githubusercontent.com/63674480/79921782-9d540200-8450-11ea-9311-a0f9cdc001d5.png"/>
</p>

Unlike the non-inverting summing amplifier, any number of voltages can be added without changing resistor values.

### 3.1.9 The Differential Amplifier

The inverting operational amplifier amplified a voltage that was applied on the inverting pin, and the output voltage was out of phase. The non-inverting pin is connected to ground with this configuration.

If the above circuit is modified by applying a voltage through a voltage divider on the non-inverting, we end up with a differential amplifier as shown below.

<p align="center">
<img src="https://user-images.githubusercontent.com/63674480/79922082-e6a45180-8450-11ea-8141-07d33b8099f7.png"/>
</p>

                                              Figure 3.7: Differential Amplifier


<p align="center">
<img src="https://user-images.githubusercontent.com/63674480/79922127-03d92000-8451-11ea-96f3-4f543e402952.png"/>
</p>

### 3.1.10 Integrator

A square wave is very easy to generate, by just toggling a GPIO of a microcontroller for example. If a circuit needs a triangle waveform, a good way to do it is just integrating the square wave signal. With an Operation Amplifier, a capacitor on the inverting feedback path, and a resistor on the input inverting pin as shown below, the input signal is integrated.

<p align="center">
<img src="https://user-images.githubusercontent.com/63674480/79923212-b8277600-8452-11ea-9829-be0c7e775be6.png"/>
</p>

                                               Figure 3.8: Integrator Amplifier

<p align="center">
<img src="https://user-images.githubusercontent.com/63674480/79923333-e9a04180-8452-11ea-93e4-8d30a7c8b22e.png"/>
</p>

Be aware that a resistor is often connected in parallel to the capacitor for saturation issues. Indeed, if the input signal is a very low frequency sine wave, the capacitor acts like an open circuit and blocks feedback voltage. The amplifier is then like a normal open-loop amplifier that has very high open-loop gain, and the amplifier is saturated. Thanks to a resistor in parallel of the capacitor, the circuit behaves like an inverting amplifier with a low frequency, and saturation is avoided.


### 3.1.11 The Differentiator Amplifier

The differentiator works similarly to the integrator by swapping the capacitor and the resistor.

<p align="center">
<img src="https://user-images.githubusercontent.com/63674480/79922847-f6706580-8451-11ea-9bf6-deece1bddb7a.png"/>
</p>

                                               Figure 3.9: Differentiator Amplifier

<p align="center">
<img src="https://user-images.githubusercontent.com/63674480/79922883-0720db80-8452-11ea-937a-45d480c13e57.png"/>
</p>

### 3.1.12 Schmitt trigger

<p align="center">
<img src="https://user-images.githubusercontent.com/63674480/79923717-c75af380-8453-11ea-8473-68b14e2bcc17.png"/>
</p>

                                             Figure 3.10: Schmitt trigger
 
 In this configuration, the input voltage is applied through the resistor R<sub>1</sub> (which may be the source internal resistance) to the non-inverting input and the inverting input is grounded or referenced. The hysteresis curve is non-inverting and the switching thresholds are ![alt text](https://user-images.githubusercontent.com/63674480/79924277-076ea600-8455-11ea-9fa0-9c78143a736c.png) where V<sub>sat</sub>  is the greatest output magnitude of the operational amplifier.

### 3.1.13 Instrumentation amplifier	

<p align="center">
<img src="https://user-images.githubusercontent.com/63674480/79923991-5d8f1980-8454-11ea-8bfb-b8f077289acc.png"/>
</p>

                                             Figure 3.11: Instrumentation amplifier	

Combines very high input impedance, high common-mode rejection, low DC offset, and other properties used in making very accurate, low-noise measurements.

It is made by adding a non-inverting buffer to each input of the differential amplifier to increase the input impedance.

### 3.1.14 Opamp as buffer

<p align="center">
<img src="https://user-images.githubusercontent.com/63674480/79281309-1d69ed00-7ed0-11ea-85f7-44c9ad8421f3.png"/>
</p>

                                             Figure 3.12: Opamp as buffer
                                                           
# SECTION 4: ACTIVE AND PASSIVE FILTERS
The filter is a circuit which changes amplitude and phase of the input signal and produces
output accordingly. It filters or eliminates some frequencies and passes some
frequencies. Hence it provides different attenuation to different frequencies. Based on
components used in the construction of the filter there are two types of filters i.e active
filter and passive filter.

**Four major types of Filters**

The four primary types of filters include the low-pass filter, the high-pass filter, the
band-pass filter, and the notch filter (or the band-reject or band-stop filter). Note: A
notch filter is a bandstop filter with a narrow bandstop bandwidth. Notch filters are
used to attenuate a narrow range of frequencies.

<p align="center">
<img src="https://user-images.githubusercontent.com/63674480/79281389-3ecad900-7ed0-11ea-8467-d8e1fadf0f9f.png"/>
</p>

                                              Figure 4.1: Types of Filters
 
 ## 4.1 Low Pass Filter
 Allows low-frequency signals and difficult passage to high-frequency signals.
 
• Inductive Low-Pass Filter

<p align="center">
<img src="https://user-images.githubusercontent.com/63674480/79281436-55713000-7ed0-11ea-96ee-7b6af18e047e.png"/>
</p>

                                               Figure 4.2: Low Pass Filter

• Capacitive Low-Pass Filter

<p align="center">
<img src="https://user-images.githubusercontent.com/63674480/79281473-6ae65a00-7ed0-11ea-923b-a9e1530facb8.png"/>
</p>

                                               Figure 4.3 Capacitive Low Pass Filter

## 4.2 High Pass Filter

Offers easy passage of a high-frequency signal and difficult passage to a low-frequency
signal.

• Inductive High Pass Filter

<p align="center">
<img src="https://user-images.githubusercontent.com/63674480/79281779-1abbc780-7ed1-11ea-85ee-1b1b618269d6.png"/>
</p>

                                                Figure 4.4: Inductive High Pass Filter

• Capacitive High Pass Filter

<p align="center">
<img src="https://user-images.githubusercontent.com/63674480/79281812-2e672e00-7ed1-11ea-966f-ea8dcd59d2bb.png"/>
</p>

                                                Figure 4.5: Capacitive High Pass Filter

## 4.3 Band Pass Filter

Combining the properties of low-pass and high-pass into a single filter creates a Band Pass Filter.

<p align="center">
<img src="https://user-images.githubusercontent.com/63674480/79281910-68d0cb00-7ed1-11ea-83af-c4e0dad5f7d0.png"/>
</p>

                                                 Figure 4.3: Band Pass Filter

## 4.4 Band Stop Filter

This kind of filter passes all frequencies above and below a particular range set by the
component values.

<p align="center">
<img src="https://user-images.githubusercontent.com/63674480/79281938-7c7c3180-7ed1-11ea-856e-b738ce577a63.png"/>
</p>

                                                Figure 4.4: Band Stop Filter

## 4.5 Passive Filter

This filter type uses passive components such as resistors (R), coils or inductors (L) and
condenser or capacitors (C) in the construction of filter. Hence it is known as passive
filter.

**Advantages**

• Cheap

• Reliable

• Easy Design

• High Efficiency

<p align="center">
<img src="https://user-images.githubusercontent.com/63674480/79282000-a7ff1c00-7ed1-11ea-8e74-28eb61a22677.png"/>
</p>

                                                  Figure 4.5: Passive Filter

## 4.6 Active Filter:

This filter type uses active components such as OP-AMP (i.e. operational amplifier) in
addition to Resistors (R) and Capacitors (C) in the construction of the filter. Hence it is
known as active filter.

**Advantages**

• No resonance issues.

• It can eliminate any harmonics

• Used for voltage regulation

• Used for reactive power compensation

• It provides reliable operation

<p align="center">
<img src="https://user-images.githubusercontent.com/63674480/79281973-91f15b80-7ed1-11ea-8553-77d71371d86d.png"/>
</p>

                                                Figure 4.6: Active Filter


**Applications**

• Radio communications: Filters enable radio receivers to only "see" the desired
signal while rejecting all other signals (assuming that the other signals have different
frequency content).

• DC power supplies: Filters are used to eliminate undesired high frequencies (i.e.,
noise) that are present on AC input lines. Additionally, filters are used on a power
supply’s output to reduce ripple.

• Analog-to-digital conversion: Filters are placed in front of an ADC input to minimize
aliasing.



                                    
