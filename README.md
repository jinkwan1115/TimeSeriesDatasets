[![Hits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2Fjinkwan1115%2FTimeSeriesDatasets&count_bg=%2379C83D&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=hits&edge_flat=false)](https://hits.seeyoufarm.com)

# TimeSeriesDatasets
This repository offers a collection of descriptions and download links for datasets related to Time Series Analysis, including tasks like forecasting, classification, and anomaly detection.

## Datasets for Time Series Forecasting
- **Six Base Datasets**
    - Electricity Transformer Temperature(ETT) datasets
        - ETTh1, ETTh2 (at 1-hour intervals)
        - ETTm1, ETTm2 (at 15-minute intervals)
    - Electricity
    - Weather
    - Exchange
    - Traffic
    - Influenza-like Illness(ILI)

- **Monash Time Series Forecasting Archive (NeurIPS 2021)**
    - https://forecastingdata.org
    - M1
        - yearly
        - quarterly
        - monthly
    - M3
        - yearly
        - quarterly
        - monthly
        - other
    - M4
        - yearly
        - quarterly
        - monthly
        - weekly
        - daily
        - hourly
    - NN5
        - daily
            - with missing values
            - without missing values
        - weekly
    - Tourism
    - CIF 2016
    - London Smart Meters
    - Australia Electricity Demand
    - Wind Farms
    - Dominick
    - Bitcoin
    - Pedestrian Counts
    - Vehicle Trips
    - KDD Cup 2018
    - Weather
    - Web Traffic
    - Solar
    - Electricity
    - Car Parts
    - FRED-MD
    - San Francisco Traffic
    - Rideshare
    - Hospital
    - COVID Deaths
    - Temperature Rain
    - Sunspot
    - Saugeen River Flow
    - US Births
    - Solar Power
    - Wind Power

## Datasets for Spatio-Temporal Analysis

## Datasets for Time Series Anomaly Detection
- **Secure Water Treatment(SWaT) dataset**
    - You need to request dataset access from iTrust Labs(https://itrust.sutd.edu.sg/itrust-labs_datasets/dataset_info/#swat)
    - This dataset is collected from a real-world water treatment plant with 7 days of normal and 4 days of abnormal operation
    - This dataset consists of sensor values (water level, flow rate, etc.) and actuator operations (valves and pumps)

- **Water Distribution(WADI) dataset**
    - You also need to request dataset access from iTrust Labs(https://itrust.sutd.edu.sg/itrust-labs_datasets/dataset_info/#swat)     
    - This is an extension of the SWaT system but had more than twice the number of sensors and actuators than the SWaT model
    - The dataset is also collected for a longer duration of 14 and 2 days of normal and attack scenarios

- **Soil Moisture Active Passive(SMAP) dataset**
    - https://nsidc.org/data/smap/data
    - Soil samples and telemetry information using the Mars rover by NASA
    - Integrated with Mars Science Laboratory(MSL) dataset in https://github.com/khundman/telemanom
    - You can get the public datasets (SMAP and MSL) on linux:
      ```
      wget https://s3-us-west-2.amazonaws.com/telemanom/data.zip && unzip data.zip && rm data.zip
      cd data && wget https://raw.githubusercontent.com/khundman/telemanom/master/labeled_anomalies.csv
      ```
    - Please refer to https://github.com/NetManAIOps/OmniAnomaly/blob/master/data_preprocess.py for preprocessing

- **Mars Science Laboratory(MSL) dataset**
    - Similar to SMAP, but corresponds to the sensor and actuator data for the Mars rover itself
    - However, this dataset is known to contain many trivial sequences, with three non-trivial ones (A4, C2 and T1)
    - [KDD 2018 paper / NASA JPL] Detecting Spacecraft Anomalies Using LSTMs and Nonparametric Dynamic Thresholding
        - https://arxiv.org/abs/1802.04431
    - [KDD 2019 paper] Robust Anomaly Detection for Multivariate Time Series through Stochastic Recurrent Neural Network
        - https://dl.acm.org/doi/10.1145/3292500.3330672

- **Server Machine Dataset(SMD)**
    - This is a five-week long dataset of stacked traces of the resource utilizations of 28 machines from a compute cluster
    - This dataset includes non-trivial sequences, specifically the traces named machine-1-1, machine-2-1, machine-3-2, and machine-3-7
    - Please refer to https://github.com/NetManAIOps/OmniAnomaly/blob/master/data_preprocess.py for preprocessing
    - [KDD 2019 paper] Robust Anomaly Detection for Multivariate Time Series through Stochastic Recurrent Neural Network
        - https://dl.acm.org/doi/10.1145/3292500.3330672

## Datasets for Time Series Classification
- **UEA Repo(Multivariate)**
    - https://www.timeseriesclassification.com
- **UCR Repo(Univariate)**
    - https://www.timeseriesclassification.com
- **UCI ML Repo**
    - Human Activity Recognition(HAR)
- **Paderborn University**
    - Machine Fault Diagnosis(MFD)
- **Sleep Stage Classification(SSC)**
