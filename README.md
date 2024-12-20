[![Hits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2Fjinkwan1115%2FTimeSeriesDatasets&count_bg=%2379C83D&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=hits&edge_flat=false)](https://hits.seeyoufarm.com)

# TimeSeries Datasets
This repository offers a collection of descriptions and download links for datasets related to Time Series Analysis, including tasks like forecasting, classification, and anomaly detection.

## Datasets for Time Series Forecasting
- **Six Base Datasets**
    - Electricity Transformer Temperature(ETT) datasets
        - ETTh1, ETTh2, ETTm1, ETTm2 (at 1-hour(or 15-minute) intervals / 6 variables / Target: 'OT')
            - HUFL / HULL
            - MUFL / MULL
            - LUFL / LULL
        
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
     
- **Numenta Anomaly Benchmark(NAB)**
    - https://github.com/numenta/NAB
    - [Neurocomputing 2017] Unsupervised real-time anomaly detection for streaming data
      - https://www.sciencedirect.com/science/article/pii/S0925231217309864
    - A dataset of multiple real-world data traces, including readings from temperature sensors, CPU utilization of cloud machines, service request latencies and taxi demands in New York city
    - However, this dataset is known to have sequences with incorrect anomaly labels such as the nyc-taxi trace
    - Real data
        - realAWSCloudwatch
            - AWS server metrics as collected by the AmazonCloudwatch service. Example metrics include CPU Utilization, Network Bytes In, and Disk Read Bytes
        - realAdExchange
            - Online advertisement clicking rates, where the metrics are cost-per-click (CPC) and cost per thousand impressions (CPM)
        - realKnownCause
            - This is data for which we know the anomaly causes; no hand labeling.
            - ambient_temperature_system_failure.csv
                - The ambient temperature in an office setting
            - cpu_utilization_asg_misconfiguration.csv
                - From Amazon Web Services (AWS) monitoring CPU usage – i.e. average CPU usage across a given cluster. When usage is high, AWS spins up a new machine, and uses fewer machines when usage is low
            - ec2_request_latency_system_failure.csv
                - CPU usage data from a server in Amazon's East Coast datacenter
                - The dataset ends with complete system failure resulting from a documented failure of AWS API servers(There's an interesting story behind this data in the Numenta blog)
            - machine_temperature_system_failure.csv
                - Temperature sensor data of an internal component of a large, industrial machine
                - The first anomaly is a planned shutdown of the machine
                - The second anomaly is difficult to detect and directly led to the third anomaly, a catastrophic failure of the machine
            - nyc_taxi.csv  ${\textsf{\color{red}(exclude this due to incorrect anomaly labels)}}$
                - Number of NYC taxi passengers, where the five anomalies occur during the NYC marathon, Thanksgiving, Christmas, New Years day, and a snow storm
                - The raw data is from the NYC Taxi and Limousine Commission
                - The data file included here consists of aggregating the total number of taxi passengers into 30 minute buckets
            - rogue_agent_key_hold.csv
                - Timing the key holds for several users of a computer, where the anomalies represent a change in the user
            - rogue_agent_key_updown.csv
                - Timing the key strokes for several users of a computer, where the anomalies represent a change in the user
        - realTraffic
            - Real time traffic data from the Twin Cities Metro area in Minnesota, collected by the Minnesota Department of Transportation
            - Included metrics include occupancy, speed, and travel time from specific sensors
        - realTweets
            - A collection of Twitter mentions of large publicly-traded companies such as Google and IBM
            - The metric value represents the number of mentions for a given ticker symbol every 5 minutes
    - Artificial data
        - artificialNoAnomaly
            - Artificially generated data without any anomalies
        - artificialAnomaly
            - Artificially generated data with varying types of anomalies

- **HexagonML/UCR Time Series Anomaly Detection Datasets**
    - https://www.cs.ucr.edu/~eamonn/time_series_data_2018/
    - 250 datasets including InternalBleeding, ECG, …
 
- **PhysioNet Open Access Databases - MIT-BIH Supraventricular Arrhythmia(MBA) Database**
    - Medicine-related datasets
    - https://physionet.org/content/svdb/1.0.0/
    - A collection of electrocardiogram recordings from four patients, containing multiple instances of two different kinds of anomalies(either supraventricular contractions or premature heartbeats)
    - [VLDB 2022 paper] TranAD: Deep Transformer Networks for Anomaly Detection in Multivariate Time Series Data
    - Please refer to https://github.com/imperial-qore/TranAD/tree/main/data/MBA

- **Multi-Source Distributed System(MSDS) Dataset**
    - https://zenodo.org/records/3549604
    - This is a recent high-quality multi-source data composed of distributed traces, application logs, and metrics from a complex distributed system
    - This dataset is specifically built for AI operations, including automated anomaly detection, root cause analysis, and remediation
    - Please refer to https://github.com/imperial-qore/TranAD/tree/main/data/MSDS

- **Synthetic Dataset from MSCRED** [MSCRED github page](https://github.com/7fantasysz/MSCRED)
    - Please refer to https://github.com/imperial-qore/TranAD/tree/main/data/synthetic
    - [AAAI 2019 paper] https://dl.acm.org/doi/10.1609/aaai.v33i01.33011409
    - Trigonometric function (C1) simulates temporal patterns (s_rand is a 0 or 1 random seed)
    - Time delay t ∈ [50, 100] and frequency ω ∈ [40, 50] (C2) simulates various periodic cycles
    - Random Gaussian noise ε ∼ N (0, 1) scaled by factor λ = 0.3 (C3) simulates data noise as well as various shapes
 
- **Yahoo S5 Dataset** [Link](https://webscope.sandbox.yahoo.com/catalog.php?datatype=s&did=70)
    - Need to request for research purpose
    - Computing Systems Data S5(A Labeled Anomaly Detection Dataset)

- **Kaggle Credit Card Fraud Detection Dataset** [Link](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)
    - The dataset contains transactions made by credit cards in September 2013 by European cardholders
    - This dataset presents transactions that occurred in two days, where we have 492 frauds out of 284,807 transactions
    - The dataset is highly unbalanced, the positive class (frauds) account for 0.172% of all transactions
 
- **HIL-based Augmented ICS (HAI) Security Dataset** [Link](https://www.kaggle.com/datasets/icsdataset/hai-security-dataset?resource=download#getting-the-dataset)
    - The HAI dataset was collected from a realistic industrial control system (ICS) testbed augmented with a Hardware-In-the-Loop (HIL) simulator that emulates steam-turbine power generation and pumped-storage hydropower generation
 
- **Drinking Water Quality Dataset(CECCO Challenge 2018)** [Link](https://www.spotseven.de/gecco/gecco-challenge/gecco-challenge-2018/)
    - For the monitoring of the water quality, the Thüringer Fernwasserversorgung performs measurements at significant points throughout the whole water distribution system, in particular at the outflow of the waterworks and the in- and outflow of the water towers
    - For this purpose, a part of the water is bypassed through a sensor system where the most important water quality indicators are measured
    - Given is the amount of chlorine dioxide in the water, its pH value, the redox potential, its electric conductivity and the turbidity of the water. These values are the water quality indicators, any changes here are considered as events
    - The flow rate and the temperature of the water is considered as operational data, changes in these values may indicate changes in the related quality values but are not considered as events themselves

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
