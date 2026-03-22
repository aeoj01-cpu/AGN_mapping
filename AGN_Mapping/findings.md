## 🔑 A. ICCF fails for short, smooth disk lags

You’ve shown:

- The disk light curve is:
    - physically correct (smoothed + delayed)
- A lag **exists (~0.2 days)**
- BUT PyCCF returns:
    - `-9999` (no detectable peak)

👉 **Conclusion:**

> Standard ICCF methods fail to recover lags when the lag is small compared to the variability timescale.

## 🔑 B. Detectability depends on relative timescales

You effectively demonstrated:

τlag≪Tvariability⇒lag not recoverable via ICCF\tau_{\text{lag}} \ll T_{\text{variability}} \Rightarrow \text{lag not recoverable via ICCF}τlag​≪Tvariability​⇒lag not recoverable via ICCF

In your case:

- lag ≈ 0.2 days
- variability features ≈ 10–100 days

👉 The signal is:

- highly correlated
- but **not measurably shifted**

---

## 🔑 C. Sampling can _destroy_ detectability

You also found:

- Original cadence → lag detectable (in principle)
- Downsampled cadence → lag disappears

👉 **Important result:**

> Time resolution must be significantly smaller than the lag to recover it.

---

## 🔑 D. Disk vs BLR behave fundamentally differently

You now have a clear contrast:

|Component|Transfer function|Lag recovery|
|---|---|---|
|BLR|narrow / peaked|easy (ICCF works)|
|Disk|broad / smooth|hard (ICCF fails)|

👉 This directly supports your project’s theme.

---

## 🔑 E. Edge effects & normalization matter (method validation)

You also solved:

- convolution edge artefacts
- continuous vs discrete normalization

👉 This validates your pipeline — very important to mention.