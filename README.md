## **Project Overview: Dataset and Objective**

The dataset for this project was provided by Maven Analytics ([Maven Commuter Challenge](https://mavenanalytics.io/challenges/maven-commuter-challenge/2300490c-532e-4f34-87a3-a47c83351164)). This challenge, titled the *Maven Commuter Challenge*, is their latest monthly competition.

The dataset includes daily ridership and traffic estimates for the Metropolitan Transportation Authority (MTA) services starting March 1, 2020, alongside percentage comparisons against pre-pandemic figures.

The objective of this project is to design an interactive dashboard that visualizes post-pandemic ridership recovery trends across MTA services.

![undefined](https://mavenanalyticsio-upload-bucket-prod.s3.us-west-2.amazonaws.com/209678157/projects/83d83da9-b771-4449-b1d3-fe7565e5f8eb.jpg)

## **Dashboard Analysis Results**  

### **Overall Recovery**  

**1.) Total Commuters (Ridership + Trips + Traffic):**

- Post-Pandemic: **7.93 billion**  

- Pre-Pandemic: **13.48 billion**  

- **Recovery Rate: 58.84%**

**2.) Total Ridership:**

- Post-Pandemic: **6.43 billion**  

- Pre-Pandemic: **11.87 billion**  

- **Recovery Rate: 54.20%**

**Service-Specific Ridership Breakdown**

**2a.) Subway:**

- Post-Pandemic: **4.28 billion**  

- Pre-Pandemic: **7.90 billion**  

**Recovery Rate: 54.17%**

**2b.) Bus:**

- Post-Pandemic: **1.72 billion**  

- Pre-Pandemic: **3.12 billion**  

- **Recovery Rate: 54.97%**

**2c.) LIRR (Long Island Rail Road):**

- Post-Pandemic: **231.95 million**  

- Pre-Pandemic: **426.73 million**  

- **Recovery Rate: 54.36%**

**2d.) MNR (Metro-North Railroad):**

- Post-Pandemic: **196.00 million**  

- Pre-Pandemic: **397.30 million**  

- **Recovery Rate: 49.33%**

**2e.) SIR (Staten Island Railway):**

- Post-Pandemic: **7.56 million**  

- Pre-Pandemic: **20.69 million**  

- **Recovery Rate: 36.53%**

**3.) AAR (Access-A-Ride) Trips:**

- Post-Pandemic: **37.43 million**  

- Pre-Pandemic: **43.38 million**  

- **Recovery Rate: 86.29%**

**4.) B&T (Bridges and Tunnels) Traffic:**

- Post-Pandemic: **1.46 billion**  

- Pre-Pandemic: **1.56 billion**  

- **Recovery Rate: 93.36%**

## **Insights from the Analysis**  

1.) **Transportation Recovery:**

- Public transit options like subways and buses are recovering at around **50%**, reflecting slower progress.  

- Transportation services such as Bridges & Tunnels (B&T) Traffic and Access-A-Ride (AAR) Trips have demonstrated faster recovery rates, reaching **90%+**.  

2.) **Notable Trends in B&T and AAR:**

- By **March 2021**, B&T traffic achieved an **87% recovery** and maintained consistency above **90%**, hitting **100.55%** in December 2022.  

- AAR recovery showed steady progress, surpassing **70%** by March 2021, and achieving **101.72% recovery** by July 2023.  

3. ) **Underperforming Services:**  

- Staten Island Railway (SIR) has struggled the most, with a **36.53% recovery rate** and monthly rates consistently below **40%**.  

4.) **Overall Recovery Gap:**

- None of the services have fully recovered when comparing cumulative post-pandemic and pre-pandemic figures. However, AAR and B&T are close to achieving full recovery, while SIR lags far behind.  

## **Recommendations**  

- **Analyze Pre- and Post-Pandemic Operations:**  

A detailed assessment of operational changes in underperforming services like SIR can inform targeted interventions to boost recovery.

- **Leverage Successful Practices:**  

Insights from the faster recovery of B&T and AAR services can be adapted to improve other transit modes.

- **Investment:**  

Invest in initiatives that enhance subway and bus ridership recovery, such as improved safety, frequency, and public awareness campaigns.

## **Data Analytics Tools and Methods**  

### **Tools Used:**  

**Microsoft Power BI:** Chosen for its seamless data transformation capabilities (via Power Query) and robust dashboard design features.

### **Data Preparation and Processing:**  

The dataset includes 15 columns (Date, 7 MTA services, and percentage comparisons to pre-pandemic figures).

![undefined](https://mavenanalyticsio-upload-bucket-prod.s3.us-west-2.amazonaws.com/209678157/projects/c9f01eb1-fc5e-462e-a00a-dfc498f13aa9.jpg)

Using **Power Query**, I calculated the Pre-Pandemic estimates for each service.

![undefined](https://mavenanalyticsio-upload-bucket-prod.s3.us-west-2.amazonaws.com/209678157/projects/5de19d21-07d7-4542-8333-d2e6755ab9ac.jpg)

I imported only the Post-Pandemic and newly calculated estimate columns into Power BI for further analysis.

This is because I no longer need the % comparison columns, and leaving them out will help the dashboard load faster.

### **Measures and KPIs:**  

Using **DAX functions**, key metrics were calculated, including but not limited to;

- Total Commuter: This is the summation of all ridership, trips, and traffic
- Total Subway Ridership
- Total Bus Ridership
- Total LIRR (Long Island Rail Road) Ridership
- Total MNR (Metro-North Railroad) Ridership
- Total AAR (Access A Ride) Trips
- Total B&T (Bridges and Tunnels) Traffic
- Total SIR (Staten Island Railway) Ridership

I calculated the same metrics for Pre-Pandemic for each MTA service and used these measures to calculate the recovery rates.

These measures were used for KPI cards and line charts to visualize trends and recovery rates.

### **Dashboard Features:**  ![undefined](https://mavenanalyticsio-upload-bucket-prod.s3.us-west-2.amazonaws.com/209678157/projects/735f958b-d41e-4a60-808f-52b7a4e887eb.jpg)

- **Trends Visualization:** Line charts display monthly trends, with drill-up (yearly) and drill-down (daily) options. The image above shows the drill-up option in action showing the yearly trend while the image below shows the drill-down option in action for daily trends in March and April 2020.![undefined](https://mavenanalyticsio-upload-bucket-prod.s3.us-west-2.amazonaws.com/209678157/projects/d4d3bcfd-d5ef-4626-aad1-44c23996696b.jpg)

- **Date Slicers:** Allow users to filter by date range or select specific months and years for detailed insights. ![undefined](https://mavenanalyticsio-upload-bucket-prod.s3.us-west-2.amazonaws.com/209678157/projects/4f2afa3f-98e7-41fe-a247-ebb559a29435.jpg)

- **KPI Cards:** Show current estimates alongside pre-pandemic figures and recovery rates, providing a clear performance overview.

## **Using the Dashboard**  

- **KPI Cards:** Highlight each service's total estimates, pre-pandemic figures, and recovery rates. The recovery rate percentage changes color depending on whether the MTA service has fully recovered.

- **Line Charts:** By default, they provide monthly trends, with drill-up and drill-down functionality. Hovering over a data point displays estimates, pre-pandemic figures, and recovery rates.  

- **Interactive Insights:** The dashboard allows users to analyze trends and performance across MTA services, offering actionable insights into recovery dynamics. 
- **Note Icons**: Some of the KPI cards have a Note icon on them that either explains what an acronym represents or how the KPI was derived.
