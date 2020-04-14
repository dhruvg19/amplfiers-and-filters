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

                              
IC 741 is widely used Op-amp. In this IC when input is zero, the output can be adjusted
to zero by varying the 10K potentiometer between offset null terminal.


### 3.1.2 Block diagram and inputs

<p align="center">
<img src="https://user-images.githubusercontent.com/63674480/79280246-8865f480-7ecd-11ea-86ad-5d4910c293a9.png"/>
</p>                                                          

An opamp has two input terminals:
1. Non-inverting input: output signal is in phase with input signal, denoted by (+).
2. Inverting input: output signal is out of phase with input signal, denoted by (-).

### 3.1.3 Non-inverting Opamp

<p align="center">
<img src="https://user-images.githubusercontent.com/63674480/79280344-c400be80-7ecd-11ea-88fb-ade10137fc83.png"/>
</p>
 
### 3.1.4 Inverting Opamp

<p align="center">
<img src="https://user-images.githubusercontent.com/63674480/79280494-1d68ed80-7ece-11ea-8bb8-1f8cbe954b41.png"/>
</p>

### 3.1.5 Opamp as buffer

<p align="center">
<img src="https://user-images.githubusercontent.com/63674480/79279637-15a84980-7ecc-11ea-9c91-2d6b1359765b.png"/>
</p>
                                                           
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
<img src="https://user-images.githubusercontent.com/63674480/79279637-15a84980-7ecc-11ea-9c91-2d6b1359765b.png"/>
</p>
 
 ## 4.1 Low Pass Filter
 Allows low-frequency signals and difficult passage to high-frequency signals.
 
• Inductive Low-Pass Filter

<p align="center">
<img src="https://user-images.githubusercontent.com/63674480/79279637-15a84980-7ecc-11ea-9c91-2d6b1359765b.png"/>
</p>

• Capacitive Low-Pass Filter

<p align="center">
<img src="https://user-images.githubusercontent.com/63674480/79279637-15a84980-7ecc-11ea-9c91-2d6b1359765b.png"/>
</p>

## 4.2 High Pass Filter

Offers easy passage of a high-frequency signal and difficult passage to a low-frequency
signal.

• Inductive High Pass Filter

<p align="center">
<img src="https://user-images.githubusercontent.com/63674480/79279637-15a84980-7ecc-11ea-9c91-2d6b1359765b.png"/>
</p>

• Capacitive High Pass Filter

<p align="center">
<img src="https://user-images.githubusercontent.com/63674480/79279637-15a84980-7ecc-11ea-9c91-2d6b1359765b.png"/>
</p>

## 4.4 Band Stop Filter

This kind of filter passes all frequencies above and below a particular range set by the
component values.

<p align="center">
<img src="https://user-images.githubusercontent.com/63674480/79279637-15a84980-7ecc-11ea-9c91-2d6b1359765b.png"/>
</p>

## 4.5 Active Filter:

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
<img src="https://user-images.githubusercontent.com/63674480/79279637-15a84980-7ecc-11ea-9c91-2d6b1359765b.png"/>
</p>

## 4.6 Passive Filter

This filter type uses passive components such as resistors (R), coils or inductors (L) and
condenser or capacitors (C) in the construction of filter. Hence it is known as passive
filter.

**Advantages**

• Cheap

• Reliable

• Easy Design

• High Efficiency

<p align="center">
<img src="https://user-images.githubusercontent.com/63674480/79279637-15a84980-7ecc-11ea-9c91-2d6b1359765b.png"/>
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



                                    
