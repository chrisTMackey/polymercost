# 🧪 polymercost

**Python tools for polymer compounding:** Calculate **Cost**, **Specific Gravity (SG)**, and estimate key **material properties** like Durometer, Modulus, and Tensile strength for compounded formulas.

---

## 💾 Installation

You can install `polymercost` using pip:

```bash
pip install polymercost
```

## 🚀 Usage
Here's a quick example of how to use the core functions:

Python
```
from polymercost import spg_costs, flex_clear_dop
```

 Define the compound formula: a list of tuples (Parts per Hundred Resin (phr), Specific Gravity (sg), Cost per pound ($))

Python
```
formula = [(100, 1.4, 0.475), (20, 2.71, 0.0625)]
```

 Calculate SG, Cost by Weight, and Cost by Volume
```
spg, cost_wt, cost_vol = spg_costs(formula)
print(f"Calculated Specific Gravity (SG): {spg:.3f}")
print(f"Cost per Weight ($/lb): {cost_wt:.4f}")
print(f"Cost per Volume ($/in³): {cost_vol:.4f}")
```

Example: Estimate properties for a clear flexible PVC compound with 50 phr DOP plasticizer

```
duro, mod, tens, elong, clash, brittle = flex_clear_dop(50)
print(f"\nEstimated Properties (50 phr DOP):")
print(f"  Durometer (Shore A): {duro}")
print(f"  100% Modulus (psi): {mod}")
print(f"  Tensile Strength (psi): {tens}")
```

## ✨ Features
spg_costs: The core function for calculating Specific Gravity, Cost/Weight, and Cost/Volume based on a compounded formula.

Property Estimators: Functions (like flex_clear_dop) to estimate properties for common polymer systems (e.g., Durometer, Tensile Strength, Elongation).

Blending Rules: Includes different blending rules for estimating properties of mixtures (e.g., arithmetic mean, log mean, inverse mean).

## 📝 License
polymercost is released under the MIT License.