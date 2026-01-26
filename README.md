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

- CKD (eGFR <60): 0.059 cm²/year lost
- Atrial fibrillation: 0.021 cm²/year lost
- Age: 0.0013 cm²/year lost per year
- LV mass index: 0.00038 cm²/year lost per g/m²
- Stroke volume index: 0.0008 cm²/year lost per mL/m²

Modifiable factors use approximate weights derived from hazard ratios in supporting studies (CANHEART 2017, Ko et al. 2022, etc.).  
Average observed decline in literature: ≈ **0.08 cm²/year** lost.

**Risk thresholds** (informed by study quartiles):
- High: > 0.12 cm²/year lost (rapid progressors)
- Medium: 0.08 – 0.12 cm²/year lost
- Low: < 0.08 cm²/year lost (slower than average)

**Important disclaimer**  
This is an **educational / research prototype**, **not** a validated clinical decision tool.  
It has **not** been prospectively validated, externally tested, or cleared by any regulatory body.  
Always interpret results with a cardiologist and use guideline-directed clinical judgment.

## Live Demo

You can try the calculator [here](https://purushothamk97.github.io/Aortic_stenosis_progression_risk_calculator/)  

### Aortic Valve Area (AVA) Reference Table

| Severity Grade       | Aortic Valve Area (AVA) | Mean Gradient (mmHg) | Peak Velocity (m/s) | Typical Clinical Notes |
|----------------------|--------------------------|-----------------------|----------------------|------------------------|
| Normal               | > 2.0 cm²               | < 10                 | < 2.0               | No stenosis            |
| Mild AS              | 1.5 – 2.0 cm²           | < 20                 | < 3.0               | Often asymptomatic     |
| Moderate AS          | 1.0 – 1.5 cm²           | 20 – 40              | 3.0 – 4.0           | Surveillance recommended |
| Severe AS            | ≤ 1.0 cm²               | ≥ 40                 | ≥ 4.0               | Consider intervention if symptomatic |
| Very Severe AS       | ≤ 0.6 cm²               | ≥ 60                 | ≥ 5.0               | High risk of events    |

**Sources**: AHA/ACC 2020 Valve Guidelines, ESC 2021 Valvular Heart Disease Guidelines
