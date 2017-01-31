---
title: Fitting Cosmic Ray Data
author: Steven Canning
---

## Introduction

## Cosmic Rays

Cosmic rays are very high energy particles with deep space origins that are detected on Earth.
Generally, only massive particles are considered cosmic rays.
We know that they originate in outer space, because their intensity increases with altitude.
Furthermore, we know that most cosmic rays are charged particles, because the intensity differs by latitude, suggesting that they are being deflected by Earth's magnetic field.

## Cosmic Ray Data

To analyze the cosmic ray data, I will use Python with the pandas, numpy, and matplotlib libraries.

First we import the file into a pandas DataFrame

```python
import pandas as pd

df = pd.read_table('cosmicrays.dat', sep='\s+')
```

To inspect the data we can use

```python
print(df.head())
```

which gives

```
    Event   Primary   E,TeV
  0    A-52    Fe      1.4 
  1    B-146   Fe      1.4 
  2    D-1-9   C      10.1 
  3    D-1-27  Ca      8.9 
  4    D-1-34  Cl     18.6 
```

A histogram of energies can also be useful.
We can generate this with the following

```python
import matplotlib
matplotlib.style.use('ggplot')
plt.figure()
df['E,TeV'].plot(kind='hist', title='Cosmic Ray Energies', bins=20)
plt.xlabel('Energy (TeV)')
```

which yields

![histogram of Energies](/images/cosmichist1.png)

## Fitting the Data

## Concluding Remarks

There is speculation about a `knee' in the energy spectrum at around 10^15 eV.
This data set does not contain enough detections at high energies to make a conclusion.

## Bibliography

Carroll, Bradley W. and Ostlie, Dale A., An Introduction to Modern Astrophysics, 2nd Ed., Pearson Education, Inc. , 2007.

C. Patrignani et al. (Particle Data Group), Chin. Phys. C, 40, 100001 (2016)

Wolchover, Natalie, The Particle That Broke a Cosmic Speed Limit, https://www.quantamagazine.org/20150514-the-particle-that-broke-a-cosmic-speed-limit/
