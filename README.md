# Aortic Stenosis Progression Risk Calculator

A simple, client-side web tool that estimates the annual decline in **Aortic Valve Area (AVA)** (cm²/year) and categorizes progression risk for patients with aortic stenosis (AS).  
Built entirely with HTML, CSS, and JavaScript — no backend or server required.

## Features

- Estimates annual AVA decline using evidence-based weights
- Categorizes risk as **Low**, **Medium**, or **High** with clinical implications
- Highlights modifiable risk factors (diabetes, hypertension, obesity, smoking, dyslipidemia)
- Displays the underlying formula and source references
- Clean, responsive, mobile-friendly interface
- 100% client-side — works offline after loading

## Scientific Basis

The core coefficients come from the 2024 multivariable linear regression model published by **Venema CS et al.** in *JACC: Advances*:

- CKD (eGFR <60): -0.059 cm²/year
- Atrial fibrillation: -0.021 cm²/year
- Age: -0.0013 cm²/year per year
- LV mass index: -0.00038 cm²/year per g/m²
- Stroke volume index: -0.0008 cm²/year per mL/m²

Modifiable factors use approximate weights derived from hazard ratios in supporting studies (CANHEART 2017, Ko et al. 2022, etc.).  
Average observed decline in literature: ≈ -0.08 cm²/year.

**Risk thresholds** (informed by study quartiles):
- High: < -0.12 cm²/year (rapid progressors)
- Medium: -0.08 to -0.12 cm²/year
- Low: > -0.08 cm²/year (slower than average)

**Important disclaimer**  
This is an **educational / research prototype**, **not** a validated clinical decision tool.  
It has **not** been prospectively validated, externally tested, or cleared by any regulatory body.  
Always interpret results with a cardiologist and use guideline-directed clinical judgment.

## Live Demo

You can try the calculator [here](https://purushothamk97.github.io/Aortic_stenosis_progression_risk_calculator/)  
