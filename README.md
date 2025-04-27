# Experimentation Examples

This repository contains Jupyter notebooks demonstrating various experimentation techniques, methodologies, and best practices.

## Overview

Experimentation is a critical part of data-driven decision making. This repository includes demonstrations of key experimentation concepts, statistical methods, and advanced design patterns.

## Sample Ratio Mismatch (SRM)

Sample Ratio Mismatch (SRM) occurs when the observed allocation of users to experiment variants differs significantly from the intended allocation. This is a critical data quality check for any experimentation program, as SRM can lead to invalid conclusions and incorrect business decisions.

The SRM demonstration notebooks include:

1. `SRM-demo.ipynb` - Comprehensive demonstration that includes:
   - Simulation of balanced and SRM-affected experiments
   - Statistical detection methods for identifying SRM
   - Visualization of how SRM impacts experiment results
   - Real-world SRM scenarios (redirect timeouts, bot traffic)
   - Evolution of SRM over time and early detection methods
   - Correction techniques for experiments with known SRM issues
   - Best practices for SRM prevention and detection

2. `SRM-simple.ipynb` - A simpler introduction to SRM concepts

3. `SRM Prevention Checklist.pdf` - A comprehensive checklist for preventing and addressing SRM issues

## Advanced Experimentation Techniques

### Sequential Testing

The `sequential_test.ipynb` notebook demonstrates sequential hypothesis testing approaches, which allow for:
- Monitoring experiments in real-time
- Making decisions as soon as sufficient evidence is available
- Reducing sample size requirements while maintaining statistical rigor
- Adapting experiment duration based on observed data

### Multi-Arm Bandit

The `multiarm_bandit.ipynb` notebook covers:
- Implementation of various bandit algorithms
- Thompson sampling and epsilon-greedy approaches
- Comparison of bandits vs. traditional A/B testing
- Techniques for balancing exploration and exploitation

### Adaptive Randomization

The `adaptive_randomization.ipynb` notebook demonstrates how to:
- Adjust treatment allocation based on observed outcomes
- Direct more traffic to better-performing variants
- Implement response-adaptive randomization
- Balance statistical power with business value

### Stepped Wedge Design

The `stepped_wedge_design.ipynb` notebook explores:
- Phased rollout experimental designs
- Cluster-based randomization approaches
- Analysis techniques for stepped implementation
- Handling time effects in gradual rollouts

## Requirements

To run these notebooks, you'll need:

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

## Getting Started

1. Clone this repository
2. Install required dependencies: `pip install -r requirements.txt`
3. Open any of the Jupyter notebooks to explore different experimentation techniques

## Why These Techniques Matter

These experimentation techniques help solve common challenges in A/B testing:

- **Sequential Testing**: Reduces experiment duration while controlling error rates
- **Multi-Arm Bandits**: Optimize for business outcomes during the experiment
- **Adaptive Randomization**: Minimizes "regret" by sending more users to better experiences
- **Stepped Wedge Design**: Enables experimentation in situations where simultaneous rollout is impractical
- **SRM Detection**: Ensures data quality and validity of experimental conclusions

## Acknowledgments

These demonstrations were inspired by real-world experimentation challenges faced by companies running large-scale experimentation programs. The code and examples are for educational purposes only.
