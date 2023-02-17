# Insightful Project Management 

Using the data provided by the bank's change requests internal web application, this project showcases how building interactive visuals can improve our internal project management process. This project aims to replace the current manual ad-hoc extraction used by the Quality & Service department in their report to top management into an actionable interface. By building a visual dashboard, executives can assess the situation and answer questions such as:  
  
- Show me the volume of projects approved in the last deployment campaign
- Show me the volume of deliverable in production at a given date
  
   
## High level architecture   
Several technologies are used to support the visual solutions. The schema below represents the process and tools required to carry the data from its source to its destination. It also present a snippet of the data architecture used in the company at the time.


![Solution architecture](/images/p5_architecture.JPG)  
  
1. *The Quality & Service Department are entering their operational data through a web-based solution.*
2. *A data ingestion pipeline gathers the raw data from the app's database and load it inside our IBM data lake.*
3. *After ingestion, our Oracle datawarehouse is retrieving the data from the data lake to load our data mart.*
4. *The data warehouse is building the data model and pushes the rows into our data mart on Postgres.*
5. *Our web-based PHP application display the interactive visuals and KPIs to end users.*

## Technological stack  
To achieve the workflow presented above, here are all the technologies I used to make it happen. Note that the stack complies with organizational rules (except for the visual libraries which fell under the governance of my department):

- The main coding language is **PHP (v7)** 
- The web application is using **Zend Framework (v3)**
- The main visuals libraries are: **D3.JS**, **Highcharts**, and **Plotly**
- Responsivity across all devices is using: **Bootstrap**
- Our events handler is **Jquery**
- Large raw data tables aesthetic comes from **DataTable**  

![Application main page](/images/p5_smartdsi_main.JPG)  
    
*The main page displays two Calendar View visuals. At the top we have the number of changes to be deployed in production at a given date. At the bottom we have the number of deliverables deployed in production at a given date.*  
    
![Detailed list](/images/p5_details.JPG)  
  
*By clicking on a cell of the Calendar View, we can have the detailed list of all the changes or deliverables deployed in production that day. It's also possible to export the needed data for further investigation on specific case.*  
  
![Plot Switch](/images/p5_switch_plot.JPG)
  
*The switch allows the user to transform the Calendar View into a monthly Bar Chart. Thanks to Plotly, we are able to also extract the visual as an image if needed.*
  
![Second Page](/images/p5_smartdsi_p2.JPG)
  
*The second tab displays the data per deployment campaigns and provides ratios regarding our ability to respect the objectives defined by the Quality & Service department.*
  
