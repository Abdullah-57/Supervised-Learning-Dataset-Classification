# Process Mining and Simulation: Manual Supervised Learning with Classification Trees

This repository contains the handwritten supervised learning classification trees. It focuses on calculating information gain to identify strong predictor attributes and constructing decision trees for predicting employee attrition based on a dataset with attributes like Job Role, Marital Status, Company Size, Job Level, and Monthly Income.

## Overview

- **Dataset Analysis**: A dataset with rows 1261-1315 (55 records). Response variable: Attrition (Stayed/Left, binary with 2 values).
- **Strong Attribute Selection**: Calculate information gain for predictor variables to identify the strongest attributes:
  - Job Role: 0.107
  - Marital Status: 0.102
  - Company Size: 0.0852
  - Job Level: 0.05
  - Monthly Income: 0.05
- **Decision Tree Construction**: Build 3 decision trees using the top attributes and compute their information gains.
- **Optimal Tree Selection**: Compare trees based on information gain to select the one with the highest predictive capability.

### Key Concepts

- **Information Gain**: Threshold set to 0.03; attributes above are considered strong.
- **Entropy Calculations**: Weighted average entropy subtracted from root entropy to get gain.
- **Tree Depth**: Up to 3 levels in examples.

## Trees Constructed

### Tree 1: Job Role → Marital Status

- Root Entropy: \~0.98
- Weighted Average Entropy: 0.629
- Information Gain: 0.351
- Depth: 2

### Tree 2: Marital Status → Job Role

- Weighted Average Entropy: 0.675
- Information Gain: 0.38 (highest)
- Depth: Not specified, but diagram shows branching.

### Tree 3: Company Size → Monthly Income → Job Level

- Weighted Average Entropy: 0.709
- Information Gain: 0.271
- Depth: 3

## Optimal Tree

- Tree 2 (Marital Status → Job Role) is selected as optimal due to the highest information gain (0.38), indicating better prediction capabilities.

## Repository Contents

- **Manual Supervised Learning with Classification Trees.pdf**: Scanned handwritten calculations, diagrams, and explanations.
- **README.md**: This file summarizing the assignment.

## How to View

- Open the PDF to view detailed handwritten notes, entropy calculations, and tree diagrams.

## Conclusion

This demonstrates manual application of the ID3 algorithm for decision tree construction, emphasizing information gain for attribute selection in predicting employee attrition. Tree 2 is optimal for its superior predictive power.