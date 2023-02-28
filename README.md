

**Introduction:**

Nepal, a South Asian country nestled between the majestic Himalayan Mountains and the lush plains of the Terai, is a land of cultural diversity and natural beauty. As a developing country, Nepal has been the subject of numerous studies and research projects that aim to understand the social, economic, and environmental challenges facing the country. In this study, I collected data from four different online sources to examine key socio-economic indicators in Nepal.

All the sources of data come from the World Bank's Open Data and the worlddata info Platforms, which provides access to a wide range of socio-economic indicators for countries around the world. The socio-economic indicators I chose for analysis were:

1) Unemployment, total (% of total labour force) <https://data.worldbank.org/indicator/SL.UEM.TOTL.ZS?locations=NP>
1) GDP (current US$) - Nepal <https://data.worldbank.org/indicator/NY.GDP.MKTP.CD?locations=NP>
1) Final consumption expenditure (% of GDP) - Nepal <https://data.worldbank.org/indicator/NE.CON.TOTL.ZS?locations=NP>
1) Historical inflation rates

<https://www.worlddata.info/asia/nepal/inflation-rates.php>

By gathering data from these four sources, the analysis aims to provide an overview of key socio-economic indicators in Nepal. Specifically, I will examine trends in the aforementioned indicators over time. The analysis will help shed light on the past and the current state of development in Nepal.![](Aspose.Words.15698e54-83ce-4db0-98d9-2bd0c7a01ffa.002.jpeg)

**Overview of the schema**

The logical schema is an essential component of any database that defines the structure and organisation of data within the system. In this schema, there are four dimension tables, named Consumption, Inflation, GDP, and Unemployment, which provide context and meaning to the data. Each dimension table contains attributes related to its respective subject area.

Additionally, there is one fact table that consolidates all the metrics from the dimension tables in one place. This fact table contains the measures or metrics that will be analysed, such as the total consumption, inflation rate, GDP growth, and unemployment rate among others.

By combining the metrics from the fact table with the attributes from the dimension tables, users can gain valuable insights into the relationships between various factors and make informed decisions based on the data.

![](Aspose.Words.15698e54-83ce-4db0-98d9-2bd0c7a01ffa.003.jpeg)

**Data cleaning and pipelining in Tableau:**

Data cleaning and pipelining are critical processes in Tableau that help to ensure accurate and reliable data analysis. Data cleaning involves the identification and removal of errors, inconsistencies, and outliers in the data, while pipelining refers to the process of transforming, filtering, and aggregating data to prepare it for analysis.

In Tableau, data cleaning and pipelining can be accomplished through various techniques and tools. For example, Tableau's data preparation tools, such as the data interpreter, can automatically detect and correct common data issues, such as misspellings and formatting errors. Additionally, Tableau's data cleansing tools, such as the cluster analysis and outlier detection, can be used to identify and remove data anomalies that can skew analysis results.

Once the data has been cleaned, pipelining can be used to transform, filter, and aggregate data to prepare it for analysis. Tableau's data blending and joining features can be used to combine data from multiple sources and create meaningful relationships between different datasets. Data blending allows data to be combined on the fly, while data joining allows data to be joined based on common fields or keys.

Overall, data cleaning and pipelining are essential components of the data analysis process in Tableau. By ensuring that data is accurate, reliable, and properly prepared, data cleaning and pipelining can help analysts to derive meaningful insights and make informed decisions based on the data.

![](Aspose.Words.15698e54-83ce-4db0-98d9-2bd0c7a01ffa.004.jpeg)

(TABLEAU FLOW FILE ATTACHED IN GITHUB)

**Data management in MICROSOFT SQL SERVER**

Microsoft SQL Server is a robust data management system that provides tools and features for organising, storing, and retrieving data in a secure and efficient manner. SQL Server supports data modelling, data integration, data warehousing, and data analysis, as well as features for managing data integrity, consolidation, and security.

![](Aspose.Words.15698e54-83ce-4db0-98d9-2bd0c7a01ffa.005.jpeg)

**(TABLE CREATION IN THE DATABASE) (Table creation code included in Github)**

**Key Performance Indicators:**

1) **How has the consumption fared in Nepal over the years?**

![](Aspose.Words.15698e54-83ce-4db0-98d9-2bd0c7a01ffa.006.jpeg)

![](Aspose.Words.15698e54-83ce-4db0-98d9-2bd0c7a01ffa.007.jpeg)

2) **What is the consumption growth rate of Nepal?**

![](Aspose.Words.15698e54-83ce-4db0-98d9-2bd0c7a01ffa.008.jpeg)

3) **What kind of growth do we see in the GDP of Nepal? Is it steady or being a developing nation, is it exponential?**

![](Aspose.Words.15698e54-83ce-4db0-98d9-2bd0c7a01ffa.009.jpeg)

4) **What is the GDP growth rate of Nepal? Has it been increasing or decreasing?**

![](Aspose.Words.15698e54-83ce-4db0-98d9-2bd0c7a01ffa.010.jpeg)

5) **Phillips curve in Nepal:** According to this theory, when GDP is high, there is low unemployment, which leads to higher wages and increased demand for goods and services. This increased demand, in turn, can lead to higher prices and inflation. Conversely, when GDP is low and unemployment is high, there is less demand for goods and services, which can lead to lower prices and deflation.

Since our datasets are dealing with vastly different value ranges, it is often necessary to scale them to enable meaningful comparison and analysis. One way to do this is to normalise the data using a common scaling technique such as **Min-Max normalisation.**

**We also need to ignore the first 31 values of unemployment because they do not exist.**

![](Aspose.Words.15698e54-83ce-4db0-98d9-2bd0c7a01ffa.011.jpeg)

Checking the Phillips curve. The data don’t seem to agree with the theory. There is no correlation.

**Summary statistics between GDP and Consumption in R:**

![](Aspose.Words.15698e54-83ce-4db0-98d9-2bd0c7a01ffa.012.png)

![](Aspose.Words.15698e54-83ce-4db0-98d9-2bd0c7a01ffa.013.png)

![](Aspose.Words.15698e54-83ce-4db0-98d9-2bd0c7a01ffa.014.png)

**Running a simple OLS linear regression in R and interpreting its coefficient estimates.**

![](Aspose.Words.15698e54-83ce-4db0-98d9-2bd0c7a01ffa.015.png)

![](Aspose.Words.15698e54-83ce-4db0-98d9-2bd0c7a01ffa.016.png)

![](Aspose.Words.15698e54-83ce-4db0-98d9-2bd0c7a01ffa.017.png)

**Interpreting goodness-of-fit metrics for OLS linear regression.**

![](Aspose.Words.15698e54-83ce-4db0-98d9-2bd0c7a01ffa.018.png)

![](Aspose.Words.15698e54-83ce-4db0-98d9-2bd0c7a01ffa.019.png)

**Relating R2 with correlation coefficient.**

![](Aspose.Words.15698e54-83ce-4db0-98d9-2bd0c7a01ffa.020.png)

![](Aspose.Words.15698e54-83ce-4db0-98d9-2bd0c7a01ffa.021.png)

**We can see that 7% of the variation in consumption of Nepal is explained by the country’s GDP.**

**Monte-Carlo Simulation:**

![](Aspose.Words.15698e54-83ce-4db0-98d9-2bd0c7a01ffa.022.png)

We can see that by simulating using Monte Carlo simulation, the parameters from the sample regression function are close to that of the true population parameters.
14
