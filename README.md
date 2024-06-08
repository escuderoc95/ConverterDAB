# Analysis and Simulation Data of a DAB Converter in Psim

## Summary

This project involves analyzing and simulating data from a Dual Active Bridge (DAB) converter using Psim. The DAB converter is a type of power converter commonly used for efficient energy transfer between two DC voltage sources. The focus of this simulation is on the transfer of energy from the low voltage side (V_L) to the high voltage side (V_H).

<div align="center">
  <img src="/results/figures/DAB.png" alt="convertidor"/>
</div>

<div align="center"> DAB converter and parameters  </div> 
<br>

## Objective

The objective of this simulation is to study the behavior and efficiency of the DAB converter under specific operating conditions, focusing on the phase shift. By analyzing the currents and voltages, we aim to better understand the converter performance, identify possible inefficiencies, and explore potential improvements.





## Parameters and Data Collected

- **Currents and Voltages**: The dataset includes various electrical parameters such as currents and voltages within the circuit.
- **Energy Transfer**: The primary objective is to analyze the energy transfer from V_L to V_H.
- **Phase Shift**: The analysis also considers the phase shift between the voltages and currents to understand its impact on the converter's performance.
- **Simulation Time**: The data was collected over a simulation period of 10 milliseconds (ms).

## Project Structure

<div align="center">
  <img src="/results/figures/lista-archivos.png" alt="convertidor"/>
</div>

<div align="center"> Project Structure  </div> 
<br>

## Preprocessing Script
The preprocessing script loads the data, performs initial statistical analysis, normalizes the data, filters it within a specific time range, and performs a linear regression analysis.

## Analysis script 
Creates various plots and saves them, along with statistical analysis results, to a PDF file.

To run the analysis script:

- Open analysis.py in your preferred IDE or text editor.

- Execute the script. In PyCharm, you can press Shift + F10 or use the run button.

## Output results

After running the scripts, you should obtain the following outputs:

Figures: Saved in the results/figures/ directory.

- Area_chart.png
- Line_chart.png
- Time_series_plot.png
- Normalized_time_series_plot.png
- PDF Report: Saved as analysis_results.pdf in the results/ directory.

The PDF report includes:

- The first few rows of the DataFrame.
- Statistics of the filtered data.
- Plots of the time series, area chart, and line chart.
- Preprocessing results, including statistical analysis and data normalization.
- Results of the linear regression analysis.

#### References

 [1] Kannan Thirugnanam, Mohamed Shawky El Moursi, Vinod Khadkikar, Hatem H. Zeineldin,
and Mohamed Al Hosani. Energy management of grid interconnected multimicrogrids
based on p2p energy exchange: A data driven approach. IEEE Transactions
on Power Systems, 36:1546–1562, 3 2021.

[2] Umamaheswararao Vuyyuru, Suman Maiti, and Chandan Chakraborty. Active power
flow control between dc microgrids. IEEE Transactions on Smart Grid, 10:5712–5723,
9 2019.

[3] Lei QIAO, Xialin LI, Di HUANG, Li GUO, Yutao XU, Zhukui TAN, and Chengshan
WANG. Coordinated control for medium voltage dc distribution centers with flexibly
interlinked multiple microgrids. Journal of Modern Power Systems and Clean Energy,
7:599–611, 5 2019.

[4] Xialin Li, Li Guo, Yunwei Li, Chao Hong, Ye Zhang, Zhen Guo, Di Huang, and
Chengshan Wang. Flexible interlinking and coordinated power control of multiple dc
microgrids clusters. IEEE Transactions on Sustainable Energy, 9:904–915, 4 2018.

[5] Eduard Bullich-Massagu´e, Francisco D´ıaz-Gonz´alez, M`onica Arag¨u´es-Pe˜nalba, Francesc
Girbau-Llistuella, Pol Olivella-Rosell, and Andreas Sumper. Microgrid clustering architectures.
Applied Energy, 212:340–361, 2 2018
## Setup and Installation

### Prerequisites

Ensure you have Python installed on your system. This project requires Python 3.6 or higher.

### Installing Dependencies

All required Python packages are listed in the requirements.txt file. To install them, follow these steps:

1. Open a terminal or command prompt.
2. Navigate to the root directory of the project where requirements.txt is located.
3. Run the following command to install the dependencies:

```sh
pip install -r requirements.txt


