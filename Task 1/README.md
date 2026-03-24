# Task 1 – Telemetry Data Analysis (Tableau)

### Goal
In May 2021, Daikibo Industrials gathered telemetry data from nine machines, across four factories worldwide.
- Daikibo Factory Meiyo – Tokyo, Japan
- Daikibo Factory Seiko – Osaka, Japan
- Daikibo Berlin – Berlin, Germany
- Daikibo Shenzhen – Shenzhen, China

Each machine sends a status message every 10 minutes. The goal was to answer two business questions:
1. In which factory did machines break down the most?
2. Which machine types broke down most often in that factory?

---

## Tools Used
- Tableau (Desktop Public Edition)

---

## Steps Taken

## 1. Data Import
- Unzipped the 'daikibo-telemetry-data.json' file after downloading it.
- Imported the JSON file into Tableau.
- Completely unpacked the nested data structure, made sure that every Schema level was examined.

### 2. Calculated Field – "Unhealthy"
- Created **Unhealthy**, a new calculated measure field.
- Logic: each message with an unhealthy status was given a value of **10** (indicating a possible downtime of ten minutes since the last message).
- Formula:
IF [Status] = "unhealthy" THEN 10 ELSE 0 END

### 3. Bar Chart – Down Time per Factory
- Made a new sheet called **Down Time per Factory**.
- The sum of the unhealthy fields for each of the four factories was plotted as the total unhealthy time.
- This graphic shows where there was the most machine downtime.

### 4. Bar Chart – Down Time per Device Type
- The second sheet was made with the title **Down Time per Device Type**.
- Plotted the overall downtime for each of the nine machine/device types.
- The most frequently failing machines are shown in the visualization.

### 5. Interactive Dashboard
- The two charts were combined into a single Tableau dashboard. 
- The **Down Time per Factory** chart were used as a filter. 
- The device type chart is dynamically updated to display only when a factory bar is selected.

### 6. Findings
- To activate the filter, one would need to click on the factory with the highest downtime.
- The second chart was updated to show the machine types that fail most frequently.
- As part of the task submission, a screenshot of the dashboard was taken and uploaded.

---

## Output

![Daikibo Dashboard](https://raw.githubusercontent.com/geralnyika/Deloitte-Data-Analytics/main/Task%201/Screenshot%20(567).png)
