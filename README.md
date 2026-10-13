# ACF & PACF Simulator

An interactive, single-page simulator for learning how ACF and PACF patterns identify simple ARIMA models. Available in English and Korean (한국어).

## Features

- Six preset models:
  - ARIMA(0,0,0): white noise
  - ARIMA(0,1,0): random walk
  - ARIMA(1,0,0) with φ₁ > 0 and with φ₁ < 0
  - ARIMA(0,0,1) with θ₁ > 0 and with θ₁ < 0
- Adjustable coefficient, series length (n = 50–1000) and number of lags (10–40)
- Differencing menu (none, 1st, 2nd) with notes on under- and over-differencing
- Time series plot plus sample ACF and PACF with ±1.96/√n significance bands
- Optional theoretical ACF/PACF markers for comparison
- A per-lag table and a short guide to reading each pattern (cut off vs. dies down)
- Light and dark mode, following the system setting

## Notes

- The MA(1) model uses the R / statsmodels sign convention: Yₜ = εₜ + θ₁εₜ₋₁. Box-Jenkins textbooks write Yₜ = εₜ − θ₁εₜ₋₁, so the sign of θ₁ is flipped there.
- The sample PACF is computed from the sample ACF with the Durbin–Levinson recursion.
- Random numbers come from a seeded generator, so the same seed and n always give the same series.

## Run locally

Open `index.html` in any modern browser. There is no build step and no dependency besides Google Fonts.

## Deploy with GitHub Pages

1. Create a new repository and upload `index.html` and `README.md` to the root.
2. Go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to *Deploy from a branch*, pick `main` and `/ (root)`, then click **Save**.
4. After a minute or two the site is live at `https://<your-username>.github.io/<repository-name>/`.
