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

                                            Figure 3.4: Inverting Opamp

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

                                            Figure 3.3: Non-inverting Opamp


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

It is worth noticing that adding several voltages is not a very flexible solution. Indeed, if a 3 <sup>rd</sup> voltage is added with exactly the same resistances, the formula would be Vs = 2/3 (V <sub>1</sub> + V <sub>2</sub> + V <sub>3</sub>).

The resistors would need to be changed to get Vs = V <sub>1</sub> + V <sub>2</sub> + V <sub>3</sub>, or a 2 <sup>nd</sup> option is to use an inverting summer amplifier.

### Inverting Summing Amplifier

By adding resistors in parallel on the inverting input pin of the inverting operation amplifier circuit, all the voltages are summed.

<p align="center">
<img src="https://user-images.githubusercontent.com/63674480/79921752-87ded800-8450-11ea-89b7-f119d5993e76.png"/>
</p>

                                             Figure 3.6: Inverting Summing Amplifier
                                             

<p align="center">
<img src="https://user-images.githubusercontent.com/63674480/79921782-9d540200-8450-11ea-9311-a0f9cdc001d5.png"/>
</p>

Unlike the non-inverting summing amplifier, any number of voltages can be added without changing resistor values.

### 3.1.7 The Differential Amplifier

<p align="center">
<img src="https://user-images.githubusercontent.com/63674480/79673112-0fc8a600-81f5-11ea-865f-62eed443b0a1.png"/>
</p>

                                              Figure 3.6: Differential Amplifier

By connecting each input in turn to 0v ground we can use superposition to solve for the output voltage Vout. Then the transfer function for a Differential Amplifier circuit is given as:

<p align="center">
<img src="https://user-images.githubusercontent.com/63674480/79673119-2111b280-81f5-11ea-8d48-c367ceb1a120.png"/>
</p>

### 3.1.8 The Differentiator Amplifier

<p align="center">
<img src="https://user-images.githubusercontent.com/63674480/79673460-8bc3ed80-81f7-11ea-9637-b7b0822f0723.png"/>
</p>

                                               Figure 3.7: Differentiator Amplifier

Since the node voltage of the operational amplifier at its inverting input terminal is zero, the current, i flowing through the capacitor will be given as:

<p align="center">
<img src="https://user-images.githubusercontent.com/63674480/79673467-9b433680-81f7-11ea-814f-f778db95d274.png"/>
</p>

The charge on the capacitor equals Capacitance times Voltage across the capacitor

<p align="center">
<img src="https://user-images.githubusercontent.com/63674480/79673472-af873380-81f7-11ea-84e0-e3685479e6a7.png"/>
</p>

Thus the rate of change of this charge is:

<p align="center">
<img src="https://user-images.githubusercontent.com/63674480/79673478-bf067c80-81f7-11ea-94b2-60dc51ceaa87.png"/>
</p>

but dQ/dt is the capacitor current, i

<p align="center">
<img src="https://user-images.githubusercontent.com/63674480/79673494-e2312c00-81f7-11ea-9e56-9550f482aeed.png"/>
</p>

from which we have an ideal voltage output for the op-amp differentiator is given as:

<p align="center">
<img src="https://user-images.githubusercontent.com/63674480/79673516-f2490b80-81f7-11ea-811f-804dca3dbe9e.png"/>
</p>

### 3.1.9 Opamp as buffer

<p align="center">
<img src="https://user-images.githubusercontent.com/63674480/79281309-1d69ed00-7ed0-11ea-85f7-44c9ad8421f3.png"/>
</p>

                                             Figure 3.8: Opamp as buffer
                                                           
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
 
 ## 4.1 Low Pass Filter
 Allows low-frequency signals and difficult passage to high-frequency signals.
 
• Inductive Low-Pass Filter

<p align="center">
<img src="https://user-images.githubusercontent.com/63674480/79281436-55713000-7ed0-11ea-96ee-7b6af18e047e.png"/>
</p>

• Capacitive Low-Pass Filter

<p align="center">
<img src="https://user-images.githubusercontent.com/63674480/79281473-6ae65a00-7ed0-11ea-923b-a9e1530facb8.png"/>
</p>

## 4.2 High Pass Filter

Offers easy passage of a high-frequency signal and difficult passage to a low-frequency
signal.

• Inductive High Pass Filter

<p align="center">
<img src="https://user-images.githubusercontent.com/63674480/79281779-1abbc780-7ed1-11ea-85ee-1b1b618269d6.png"/>
</p>

• Capacitive High Pass Filter

<p align="center">
<img src="https://user-images.githubusercontent.com/63674480/79281812-2e672e00-7ed1-11ea-966f-ea8dcd59d2bb.png"/>
</p>

## 4.3 Band Pass Filter

Combining the properties of low-pass and high-pass into a single filter creates a Band Pass Filter.

<p align="center">
<img src="https://user-images.githubusercontent.com/63674480/79281910-68d0cb00-7ed1-11ea-83af-c4e0dad5f7d0.png"/>
</p>

## 4.4 Band Stop Filter

This kind of filter passes all frequencies above and below a particular range set by the
component values.

<p align="center">
<img src="https://user-images.githubusercontent.com/63674480/79281938-7c7c3180-7ed1-11ea-856e-b738ce577a63.png"/>
</p>

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


**Applications**

• Radio communications: Filters enable radio receivers to only "see" the desired
signal while rejecting all other signals (assuming that the other signals have different
frequency content).

• DC power supplies: Filters are used to eliminate undesired high frequencies (i.e.,
noise) that are present on AC input lines. Additionally, filters are used on a power
supply’s output to reduce ripple.

• Analog-to-digital conversion: Filters are placed in front of an ADC input to minimize
aliasing.



                                    
