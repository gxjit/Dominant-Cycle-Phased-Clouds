# Dominant Cycle Phased Clouds

Welcome to the documentation for the **Dominant Cycle Phased Clouds** indicator. This tool leverages advanced Digital Signal Processing (DSP) to dynamically adjust to the market's true rhythm. Instead of relying on static, arbitrary lookback periods (like a traditional 50 or 200-period moving average), this indicator constantly measures the market's dominant cycle and mathematically scales its moving average clouds to stay perfectly in phase with the market.

This indicator is heavily inspired by the pioneering DSP work of **John Ehlers**, specifically utilizing his Autocorrelation Periodogram (ACP) for cycle measurement and his SuperSmoother filters for lag-free price smoothing, combined with the visual and strategic framework of moving average clouds popularized by **Ripster**.

---

## For Traders: How to Read & Use

At its core, this indicator plots two distinct, color-coded bands (clouds) on your chart. Because these clouds are tied to the market's live dominant cycle, they expand, contract, and shift dynamically as market dynamics and cycle lengths change.

### The Two Clouds

* **Inner Cloud (Short-Term Momentum):** Represents the relationship between a sub-harmonic cycle and the primary dominant cycle. It is highly reactive and excellent for identifying immediate trend shifts and short-term momentum entries.
* **Outer Cloud (Macro Trend):** Represents the relationship between the dominant cycle and a larger super-harmonic cycle. It filters out the noise and defines the broader structural trend.

### Trading Signals

* **Trend Alignment:** When both the Inner and Outer clouds are the same color (e.g., Bullish), the market is in a synchronized, strong trend.
* **Pullbacks & Value Zones:** During a strong Outer Cloud trend, pullbacks into the Inner Cloud often represent high-probability entries.
* **Phase Shifts (Reversals):** If the Inner Cloud crosses through the Outer Cloud or changes color, it is an early warning of a trend reversal.

### Settings Guide

| Setting | Description | Recommendation |
| --- | --- | --- |
| **Min/Max Dominant Cycle** | The boundaries within which the algorithm searches for the market's heartbeat. | Default (**8** to **48**) covers most standard trading cycles. Expand if trading very high timeframes. |
| **MA Type** | The smoothing algorithm used to render the clouds. Options include SSF, EMA, SSF3, EMA2. | **SSF (SuperSmoother)** is highly recommended for its superior ability to eliminate lag while dropping high-frequency noise. |
| **Expansion Multiplier** | The harmonic ratio used to space out the cloud boundaries. | **1.6** (Golden Ratio) for natural scaling. **1.414** for strict half octave separation. |

---

## 📜 Acknowledgements & Credits

* **John F. Ehlers:** For his decades of contribution to technical analysis, introducing the Autocorrelation Periodogram, the SuperSmoother filter, and operationalizing the use of DSP in trading.
* **Ripster (@ripster47):** For conceptualizing and popularizing "Ripster Clouds" (EMA clouds). The visual representation and core trading application of using layered, color-coded moving average bands to define trend structure and dynamic support/resistance zones were heavily inspired by his methodology.
* **mihakralj (QuanTAlib):** For the highly optimized, O(n) Pine Script implementation of the Autocorrelation Periodogram dominant cycle estimator used as the analytical engine in this code.
