This is a single note.

Not a folder full of things.

It contains:

- What the project is doing
    
- Current question
    
- Confirmed results
    
- Open problems
    

## Stage 1: Validate the code

Create a notebook called

```
01_Verification.ipynb
```

Record things like

- sinusoid lag recovery
- PSD light curve generation
- transfer function normalization
- convolution correctness
- CCF centroid vs true lag
- Fourier lag vs true lag

Every figure should have

- caption
- explanation
- conclusion

This becomes Appendix A in your report.

---

## Stage 2: Disk-only simulations

Create

```
02_DiskParameterStudy.ipynb
```

Now systematically vary

- wavelength
- BH mass
- accretion rate
- inclination (if possible)

For each simulation save

- transfer function
- light curves
- CCF
- lag-frequency spectrum
- mean lag

Then make summary plots

```
τ(f)
```

for multiple wavelengths.

This directly demonstrates radial dependence.

---

## Stage 3: BLR-only simulations

```
03_BLRParameterStudy.ipynb
```

Vary

- BLR width
- mean lag
- response width
- asymmetry

Study

How does

```
τ(f)
```

change?

Where does flattening occur?

Where does coherence decrease?

This tells you how BLR geometry affects observations.

---

# Stage 4 (MOST IMPORTANT)

## Mixed Disk + BLR

This is where I think your project becomes genuinely interesting.

Create

```
04_MixedResponse.ipynb
```

Now vary

BLR fraction

from

```
0%10%20%30%...100%
```

Everything else fixed.

Measure

- CCF
- frequency lags
- phase lags
- coherence

Plot

```
τ(f)
```

for each BLR fraction.

This is probably your strongest figure.

---

Then repeat for

different wavelengths.

Now you have

```
τ(f,λ)
```

instead of

```
τ(f)
```

This is much richer scientifically.

---

# Stage 5

Produce contour plots.

For example

x-axis

frequency

y-axis

BLR fraction

colour

lag

Like

```
BLR%100 |************* 80 |******** 60 |****** 40 |**** 20 |**  0 |*    ----------------      frequency
```

This would immediately show how contamination affects observed lags.

Even better:

frequency vs wavelength.

---

# Stage 6

Compare simulations against NGC4151.

Instead of saying

> "The lag decreases."

say

> "The observed lag-frequency spectrum most closely matches simulations with approximately X% BLR contamination."

That is an actual scientific result.
# AGN Reverberation Mapping Project  

## Core Aim  
Can frequency-resolved UV/optical lags reliably recover disk and BLR contributions under realistic sampling?
  
## Confirmed  
- PYCCF works for noise-free data - specifically using BLR tansfer function we found using a disk function the lag was too small in comparison to the variability to be recovered.  
- Centroid lag differs from analytic mean due to response width, we see different variatins over the BLR and disk functions .  
- found a new method to find mean lag which is  more comparable to the PYCCF lag to allow us to compare using the CCF 
- compared the three different types of lags for the disk and blr 
  
## Current Issue  
- .  write up report on the blr lags 
- fond the three types of lags for the blr and disk at 0.5 
- try and find a measure of certainty 
- do this for different blr fractions 
- run in extreme conditions 
- turn into pipeline 
  
## Next Steps  
- Verify that your simulation pipeline produces physically correct and unbiased frequency-resolved lags.

You update this every few days.

This keeps your thinking focused.