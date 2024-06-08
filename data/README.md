# Data Directory

## Summary

This directory contains the raw simulation data for the DAB converter analysis project. The data is essential for performing statistical analysis, normalization, visualization, and regression modeling as part of the project.

## Datos de la tabla

A continuación se presenta una tabla que muestra valores de tiempo y mediciones de diferentes variables.

| Time     | I_LK     | VHigh    | Vlow     | VLK      |
|----------|----------|----------|----------|----------|
| 0.000000 | 0.497729 | 0.000077 | 0.000000 | 0.500001 |
| 0.000005 | 0.497738 | 0.000077 | 0.018167 | 0.500756 |
| 0.000010 | 0.497758 | 0.000077 | 0.036276 | 0.501509 |
| 0.000015 | 0.497788 | 0.000077 | 0.054353 | 0.502260 |
| 0.000020 | 0.497829 | 0.000077 | 0.072389 | 0.503009 |


## Files

### `simulacion_VLVHresistencia110.txt`

This text file contains the raw simulation data for the DAB converter. The data is tab-delimited and includes the following columns:

- **Time**: Time in seconds (s)
- **I_LK**: Leakage current in amperes (A)
- **VHigh**: High voltage side voltage in volts (V)
- **Vlow**: Low voltage side voltage in volts (V)
- **VLK**: Leakage voltage in volts (V)

## Data Description

The simulation data captures the behavior of the DAB converter over a period of 10 milliseconds (ms). The primary focus is on analyzing the transfer of energy from the low voltage side (V_L) to the high voltage side (V_H), considering the phase shift between voltages and currents.

### Columns

1. **Time**: This column records the simulation time in seconds.
2. **I_LK**: This column records the leakage current in amperes.
3. **VHigh**: This column records the voltage on the high voltage side in volts.
4. **Vlow**: This column records the voltage on the low voltage side in volts.
5. **VLK**: This column records the leakage voltage in volts.

## How to Use the Data

### Loading the Data

To load the data into a pandas DataFrame for analysis, use the following code:

```python
import pandas as pd
import os

data_file = os.path.join(os.path.dirname(__file__), 'simulacion_VLVHresistencia110.txt')
df = pd.read_csv(data_file, delimiter='\t', names=['Time', 'I_LK', 'VHigh', 'Vlow', 'VLK'])
