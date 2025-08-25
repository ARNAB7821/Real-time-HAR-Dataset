**Data Collection Tools:**
           All the volunteers used their own smartphones for collecting data. The configuration of all the smartphones is different, and each contains the Android operating system.
           Due to the variation in hardware components and different smartphone brands, the collected data may vary slightly. Each smartphone contains the software G-sensor Logger for 
           collecting activities data. 

**G-sensor Logger:** 
           It captures accelerometer (G-sensor) data and logs it to CSV files, calculates magnitude, minimum & maximum values, and offers playback of recorded data.
           Sudden changes in motion can be detected and recorded using the G-sensor. By default, it usually records at the 50 Hz sampling rate. 

**Data Collection Procedure:**
          All the volunteers individually recorded their five activities on the smartphone. First, they started the G-sensor logger apps and kept their phone in their pants pocket. Then, they started to perform 
          every single activity for five minutes. After five minutes, they stopped the data recording and saved the .csv file. In this way, they recorded all five activities and merged all the .csv files into a             single and complete dataset.

**Sampling the dataset:**
          All five activities of six volunteers for five minutes contain a large amount of data for decentralised federated learning processing. For this reason, we used the sampling technique to reduce the                 number of records in the dataset. The total number of records in the sampling dataset is 22500 (But here we are given a subset of the sampling dataset; the full dataset will be provided on demand).  

**Labeling the dataset:**
          The G-sensor logger apps record data of 9 feature columns, including time series values. The names of the features are Time, Acceleration along the X-axis(m/s²), acceleration along the Y-axis(m/s²),               acceleration along the Z-axis(m/s²), Magnitude,  minimum acceleration along the X-axis(m/s²), minimum acceleration along the Y-axis(m/s²), minimum acceleration along the Z-axis(m/s²), and minimum                  Magnitude. Those feature column names are represented by 'Time (s)', 'X', 'Y', 'Z', 'V', 'MAx', 'MAy', 'MAz', 'MAv'. We added a column in the dataset named 'Activity'. We labeled five activities as 
          lying as label 0, running as label 1, sitting as label 2, standing as label 3, and walking as label 4. In the dataset total number of samples for lying activity is 4394, total number of samples for                running activity is 4427, total number of samples for sitting activity is 4626, total number of samples for standing activity is 4535, and total number of samples for walking activity is 4518.  

**Data preprocessing:**
          We applied several data preprocessing mechanisms to the whole dataset to improve the accuracy. For data cleaning, we applied the mean and median for handling missing or null values. We applied the Z-              score normalization to remove outliers and avoid redundancy. For feature engineering, we applied resampling, mean and variance. For data balancing, we applied the SMOTE function to resolve oversampling            or undersampling.
          
But after applying all the procedures, the accuracy of this dataset using DFL near about 84% which is quite lower than the existing benchmark human activity datasets because of several limitations during data collection. The number of features are only five, the placement of the smartphone during data collection was not always fixed, the number of volunteers was also not as many as expected, etc are the major reasons for the low accuracy. In the future, we must try to overcome all these limitations.  





         


