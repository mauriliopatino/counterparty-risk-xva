# Sample class — What is your counterparty's promise to pay worth?

Material from a promotional sample class for the Maestría en Administración de Riesgos,
Universidad Anáhuac. Every item is available in **English (`_ENG`)** and **Spanish (`_ESP`)**;
the class was delivered in Spanish.

| Item | English | Español |
|---|---|---|
| Slides (20 frames, ~33 min) | [`slides_ENG.pdf`](slides_ENG.pdf) | [`slides_ESP.pdf`](slides_ESP.pdf) |
| Live demo notebook | [`cva_dva_demo_ENG.ipynb`](cva_dva_demo_ENG.ipynb) | [`cva_dva_demo_ESP.ipynb`](cva_dva_demo_ESP.ipynb) |
| Lecture notes (14 pages) | [`lecture_notes_ENG.pdf`](lecture_notes_ENG.pdf) | [`lecture_notes_ESP.pdf`](lecture_notes_ESP.pdf) |

Run the notebook in the browser, nothing to install:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/mauriliopatino/counterparty-risk-xva/blob/main/sample-class/cva_dva_demo_ENG.ipynb)
· English

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/mauriliopatino/counterparty-risk-xva/blob/main/sample-class/cva_dva_demo_ESP.ipynb)
· Español

## What the demo covers

1. **Simulating the future** — 10,000 paths of the TIIE de Fondeo short rate under $\mathbb{Q}$
   with a calibrated two-factor Gaussian model (G2++). Exact scheme, no discretisation error.
2. **Pricing the swap** in every scenario with the closed-form zero-coupon bond formula.
3. **The distribution split at zero** — where CVA and DVA come from: two sides of one coin.
4. **The exposure hump** and its negative mirror image.
5. **The price** — CVA, DVA and bilateral netting, including the break-even point where the
   adjustment changes sign.
6. **One swap, six counterparties** — the price of risk changes by a factor of seven.
7. **Monte Carlo convergence** — why the engine is expensive: the error decays as $1/\sqrt{N}$.
8. **The machine learning surrogate** — trained on labels from the engine itself.
9. **The race** and a real-time pre-deal quote, reconciled against the engine.

## Notes

The notebook runs end to end in about 30 seconds on a standard laptop. `xgboost` is optional: if
it is not installed, the notebook falls back automatically to scikit-learn's
`HistGradientBoostingRegressor`.

**Simplifications made so the demo runs live:** a flat curve at the level of TIIE de Fondeo and
quarterly payment dates. With the full Valmer curve and the fine time grid, the CVA of the
reference swap is 5.55 bps.

Figure axis labels inside the lecture notes are in Spanish: they are reproduced from the source
thesis without modification.
