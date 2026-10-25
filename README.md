# STORM Leverage Studio

A lightweight, browser-based leverage calculator for estimating theoretical leverage from entry price, stop price, trading fees, and maintenance margin.

The interface is in Persian (Farsi) and uses a right-to-left layout.

## Features

- Calculates theoretical leverage using entry and stop prices.
- Automatically identifies the position direction (long or short) from the entered prices.
- Accounts for entry fees, exit fees, and maintenance margin in a simplified isolated-margin model.
- Lets you set minimum and maximum leverage bounds.
- Shows stop distance, round-trip fees, raw leverage, and the bounded result.
- Includes synchronized entry/exit fee inputs, reset controls, and a light/dark theme toggle.
- Responsive layout for desktop and mobile.
- Runs entirely in the browser; no backend or API keys are required.

## Run locally

1. Download or clone this repository.
2. Open `index.html` in a modern web browser.

No package installation or build process is needed.

## Deploy for free with GitHub Pages

1. Create a GitHub repository named `storm-leverage-studio` (or another name you prefer).
2. Upload `index.html` and `README.md` to the repository's root directory.
3. In the repository, open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select the `main` branch and the `/ (root)` folder, then save.
6. Wait for GitHub Pages to publish the site. The URL will be shown in the Pages settings and will usually look like:

   `https://YOUR-USERNAME.github.io/storm-leverage-studio/`

If you name the repository `YOUR-USERNAME.github.io`, the site can instead be published at `https://YOUR-USERNAME.github.io/`.

## Calculation model

The calculator uses this simplified model:

`L = 1 / [d + fᵢ + (S / E) × (fₒ + m)]`

Where:

- `L` = raw theoretical leverage
- `E` = entry price
- `S` = stop/liquidation reference price
- `d = |E − S| / E` = relative distance between entry and stop
- `fᵢ` = entry fee rate as a decimal
- `fₒ` = exit fee rate as a decimal
- `m` = maintenance margin rate as a decimal

The displayed leverage is clamped to the configured minimum and maximum. Fee and maintenance-margin inputs are entered as percentages in the UI.

## Important disclaimer

This tool provides estimates for educational and planning purposes only. It does not guarantee an exchange's actual liquidation price or a safe leverage level. Exchange-specific contract rules, maintenance-margin tiers, funding, slippage, liquidation fees, and other factors may change real outcomes. Verify contract specifications with your exchange and make independent risk decisions.

## License

MIT - Hmmm
