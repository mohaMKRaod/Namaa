# Road Defect Detection Pipeline
## Project Overview

This project presents a data pipeline designed to efficiently process visual data collected from 360-degree road scanners. The pipeline incorporates human expertise and AI to accurately identify and annotate visual polutions like damged fances or broken light poles or wall gravite the problem had more than 70 defect to be labeld .

### Key Features

- **Data Ingestion**: Seamlessly integrates visual data from multiple 360-degree road scanners.
- **Human-in-the-Loop**: Combines human expertise with AI for accurate defect detection.
- **AI-Powered Annotation**: Utilizes YOLOv8 to automatically annotate images, reducing manual effort.
- **Quality Control**: Enables engineers to review and correct AI-generated annotations with the appilty to do modifications on them.
- **GIS Integration**: Conecting the gps data that were collected from the road scaner to Visualizes and analyzes results on interactive maps, providing insights at various geographic levels.
- **Streamlit Interface**: Offers a user-friendly interface for data exploration and visualization.
- **The integration with c# ui**: for commercial use we needed to integrate the system with a C# frame for production and to add the system as a SaaS model using postgresql.
### Technologies
Streamlit
YOLOv8
Labelme
GIS (GeoPandas, ArcPy,pydeck)
Docker
pandas 
postgresql


![Pipeline Overview](images\Pipline.jpeg)

## Results
### Before building the pipeline

* To label 600 images and extract the defects from them and label them from 30 defects it took around 3 months and there was a lot of delay because of the different point of view between the labeling who were domain experts in the field  
* The class disruption was heavenly imbalanced- The benchmark for the init model was around 60% map(mean average precision)
* ### After building the pipeline
* it takes around 5 minutes to label 300 hundred images and around 1 week to fix the mislabeled data and because of the Human-in-the-Loop the accuracy of the model increased with time and the time needed to fix the mislabeled data had shrunk.
* because of the flexibility we were able to increase the number of defects from 30 to 71 without having issues 
* the accuracy of the model jumped from 60% map to 87% map 
* adding the GIS data gives the ability to add more business values by classifying each part in KSA by the number of defects and applying penalties on the business owners who don't fix these defects plus giving the government the ability to make a dissection witch part to start to fix first
