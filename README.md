# Counterparty Risk & XVA — A Practitioner's Series

**Maurilio Patiño García**

Technical notes and Python notebooks on counterparty credit risk and valuation adjustments, built
around the Mexican interest rate market. The series covers the full chain: term structure models
and their calibration, Monte Carlo exposure simulation, credit curves from CDS, CVA and DVA, and
machine learning surrogates for portfolio-scale computation.

This is the risk-neutral counterpart to
[credit-risk-modeling](https://github.com/mauriliopatino/credit-risk-modeling), which covers
credit portfolio risk under the physical measure. Here the question is not *how likely is default*
but *what does the promise to pay cost today*.

## Contents

| # | Topic | Format | Link |
|---|-------|--------|------|
| 1 | What is your counterparty's promise to pay worth? CVA and DVA with simulation and machine learning | Slides + Notebook + Notes | [Slides](sample-class/presentation.pdf) · [Notebook](sample-class/cva_dva_demo.ipynb) · [Notes](sample-class/lecture_notes.pdf) |

Open the notebook in the browser, no installation required:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/mauriliopatino/counterparty-risk-xva/blob/main/sample-class/cva_dva_demo.ipynb)

## In preparation

- The G2++ model: step-by-step derivation, closed-form bond and swaption pricing, calibration to
  the ATM swaption surface.
- PCA of the TIIE de Fondeo curve: level, slope and curvature, and how they map to a two-factor
  short rate model.
- Bootstrapping credit curves from CDS spreads: hazard rates, survival probabilities and proxy
  curves for counterparties without quoted CDS.
- Exposure profiles under netting and collateral: EE, ENE, PFE, and the effect of CSA thresholds.
- Machine learning surrogates for CVA: dataset design, model families, and why the choice depends
  on whether you need levels or sensitivities.
- Incremental CVA for pre-deal quoting, and Euler allocation of portfolio CVA to individual
  trades.
- Wrong-way risk: measuring the interaction between exposure and credit quality.
- The Mexican regulatory chain: IFRS 13, NIF C-10, Anexo 33 CUB (CNBV), Formulario XVA (Banxico),
  and BIS MAR 50 — and why accounting CVA and regulatory CVA capital must not be conflated.

## Notes on the material

All market data is attributed to **Valmer**, with a reference date of 24 March 2026. Portfolios
used in the examples are synthetic, designed to carry plausible features of a Mexican interest
rate book without reproducing any specific institution's positions.

Most of this material derives from the master's thesis *«Comparación de métodos numéricos para el
cálculo de CVA en swaps de tasas de interés: Monte Carlo, aproximaciones analíticas y aprendizaje
automático»*, Maestría en Métodos Matemáticos en Finanzas, Universidad Anáhuac.

## References

### Books

- J. Gregory. "Counterparty Credit Risk and Credit Value Adjustment: A Continuing Challenge for
  Global Financial Markets". Wiley, 2nd ed., 2012.
- A. Green. "XVA: Credit, Funding and Capital Valuation Adjustments". Wiley, 2015.
- D. Brigo, F. Mercurio. "Interest Rate Models — Theory and Practice: With Smile, Inflation and
  Credit". Springer, 2nd ed., 2006.
- D. Brigo, M. Morini, A. Pallavicini. "Counterparty Credit Risk, Collateral and Funding: With
  Pricing Cases for All Asset Classes". Wiley, 2013.
- T. R. Bielecki, M. Jeanblanc, M. Rutkowski. "Credit Risk Modeling". Osaka University Press, 2009.
- P. Glasserman. "Monte Carlo Methods in Financial Engineering". Springer, 2003.
- A. Savine. "Modern Computational Finance: AAD and Parallel Simulations". Wiley, 2018.

### Papers

- F. A. Longstaff, E. S. Schwartz. "Valuing American Options by Simulation: A Simple Least-Squares
  Approach". The Review of Financial Studies, 14(1):113–147, 2001.
- M. Giles, P. Glasserman. "Smoking Adjoints: Fast Monte Carlo Greeks". Risk, 19(1):88–92, 2006.
- R. Litterman, J. Scheinkman. "Common Factors Affecting Bond Returns". The Journal of Fixed
  Income, 1(1):54–61, 1991.
- B. Huge, A. Savine. "Differential Machine Learning". SSRN preprint, 2020.
- S. Crépey, M. F. Dixon. "Gaussian Process Regression for Derivative Portfolio Modeling and
  Application to CVA Computations". Journal of Computational Finance, 24(1):47–81, 2020.
- K. Andersson, C. W. Oosterlee. "Deep Learning for CVA Computations of Large Portfolios of
  Financial Derivatives". Applied Mathematics and Computation, 409:126399, 2021.
- A. Gnoatto, A. Picarelli, C. Reisinger. "Deep xVA Solver: A Neural Network-Based Counterparty
  Credit Risk Management Framework". SIAM Journal on Financial Mathematics, 14(1):314–352, 2023.
- L. A. Abbas-Turki, S. Crépey, B. Saadeddine. "Pathwise CVA Regressions with Oversimulated
  Defaults". Mathematical Finance, 33(2):274–307, 2023.
- M. Silotto, M. Scaringi, M. Bianchetti. "Everything You Always Wanted to Know About XVA Model
  Risk but Were Afraid to Ask". Annals of Operations Research, 336:183–274, 2024.
- T. Chen, C. Guestrin. "XGBoost: A Scalable Tree Boosting System". KDD '16, 785–794, 2016.

### Regulatory Documents

- IASB. "IFRS 13: Fair Value Measurement".
- CNBV. "Disposiciones de carácter general aplicables a las instituciones de crédito", Anexo 33,
  criterio B-5.
- Banco de México. "Formulario XVA — Ayudas genéricas".
- Banco de México. "Circular 4/2012".
- Basel Committee on Banking Supervision. "MAR 50: Credit Valuation Adjustment Risk". BIS.

## License

Code is released under the [MIT License](LICENSE). Technical notes (PDFs) are shared under
[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/): feel free to use them with attribution.
All material is provided as-is, for educational purposes, with no warranty. Nothing here
constitutes investment advice or a valuation recommendation for professional use.
