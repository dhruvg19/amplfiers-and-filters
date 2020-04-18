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
                                              
                                          Figure 21: schematic symbol of Op-amp

                              
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


### 3.1.3 Block diagram and inputs

<p align="center">
<img src="https://user-images.githubusercontent.com/63674480/79671259-d2f5b280-81e6-11ea-9e0f-d6dd67df44dd.png"/>
</p>         

                                           Figure 22: Block diagram of Opamp

An opamp has two input terminals:
1. Non-inverting input: output signal is in phase with input signal, denoted by (+).
2. Inverting input: output signal is out of phase with input signal, denoted by (-).

### 3.1.4 Non-inverting Opamp

<p align="center">
<img src="https://user-images.githubusercontent.com/63674480/79280344-c400be80-7ecd-11ea-88fb-ade10137fc83.png"/>
</p>

                                            Figure 23: Non-inverting Opamp
 
### 3.1.5 Inverting Opamp

<p align="center">
<img src="https://user-images.githubusercontent.com/63674480/79280494-1d68ed80-7ece-11ea-8bb8-1f8cbe954b41.png"/>
</p>

                                            Figure 24: Inverting Opamp

### 3.1.6 Opamp as buffer

<p align="center">
<img src="https://user-images.githubusercontent.com/63674480/79281309-1d69ed00-7ed0-11ea-85f7-44c9ad8421f3.png"/>
</p>

                                             Figure 25: Opamp as buffer
                                                           
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



                                    
