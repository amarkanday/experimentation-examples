# Sample Ratio Mismatch (SRM) Demonstration

This repository contains a Jupyter notebook that demonstrates how Sample Ratio Mismatch (SRM) affects A/B testing and experimentation.

## Overview

Sample Ratio Mismatch (SRM) occurs when the observed allocation of users to experiment variants differs significantly from the intended allocation. This is a critical data quality check for any experimentation program, as SRM can lead to invalid conclusions and incorrect business decisions.

This demonstration notebook includes:

1. Simulation of balanced and SRM-affected experiments
2. Statistical detection methods for identifying SRM
3. Visualization of how SRM impacts experiment results
4. Real-world SRM scenarios (redirect timeouts, bot traffic)
5. Evolution of SRM over time and early detection methods
6. Correction techniques for experiments with known SRM issues
7. Best practices for SRM prevention and detection

## Requirements

To run this notebook, you'll need:

```
numpy==1.24.3
pandas==2.0.2
matplotlib==3.7.1
scipy==1.10.1
seaborn==0.12.2
jupyter==1.0.0
ipykernel==6.23.1
statsmodels==0.14.0
```

Install the dependencies via:

```bash
pip install -r requirements.txt
```

## Key Features

### SRM Detection

The notebook demonstrates various methods for detecting SRM:
- Chi-square test for comparing observed vs. expected ratios
- Continuous monitoring for early detection
- Segment-level analysis to isolate affected user groups

### Real-World SRM Scenarios

Simulations of common SRM causes:
- Redirect timing issues affecting mobile users
- Browser compatibility problems
- Bot traffic skewing variant distributions
- Performance differences between variants

### SRM Prevention Best Practices

Comprehensive checklist for preventing and addressing SRM:
- Pre-launch checks
- Experiment monitoring
- Technical implementation best practices
- Team protocols

## Getting Started

1. Clone this repository
2. Install required dependencies: `pip install -r requirements.txt`
3. Open the Jupyter notebook: `jupyter notebook SRM_Demonstration.ipynb`

## Why SRM Matters

Even a small SRM can have significant impact on experiment conclusions. This demonstration shows how:
- SRM can lead to false positives or false negatives
- Different user segments can be affected differently
- SRM can evolve over time, making early detection crucial
- Proper correction methods can salvage valuable experiment data

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

This demonstration was inspired by real-world experimentation challenges faced by companies running large-scale A/B testing programs. The code and examples are for educational purposes only.
