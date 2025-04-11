# DISCOSweb ETL pipeline

The following repository presents a use case ETL pipeline that downloads data from the DISCOS database 
through the DISCOSWeb API.  
All information available at [DISCOS website](https://discosweb.esoc.esa.int/).  
The repository contains:
* **ecosmic.ipynb** jupyter notebook;
* **raw_data_filtered.json** file that presents downloaded and filtered data through the API in JSON format;
* **token.env** sample file to set the environment variable of the API access token.  


___NOTE:___    
_The user should update the **token.env** file with her own API access token in order to download data.
Insert it in the appropriate **.gitignore** file before committing._

The **ecosmic.ipynb** is divided into the following sections:  
### DATA EXTRACTION & FILTERING
- Request through the API is sent such that downloaded data are filtered
so as to consider only objects with reentry epoch after _2025-01-01_ and with _mass!=0_;
- Downloading excludes _relationships_ and _links_;
- Downloaded data are saved in a JSON file.
### DATA TRANSFORMATION & VISUALIZATION
- **Transformin data** - In this section data are transformed into a suitable format for analysis
and, thus, cleaned and stored in a _.csv file_;
- **Data Analysis & Visualization** - In this section data are loaded as in a dataframe and objects
  are categorized into their shape and analyzed with a specific focus on one of their dimensions.

__FUTURE IMPLEMENTATION:__  
_Future work should focus on extracting more meaningful insights related to the specific ambit
of collision alerts._

