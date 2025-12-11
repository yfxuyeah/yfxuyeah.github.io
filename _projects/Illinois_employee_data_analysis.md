---
name: State Employee Pay Data Analysis
tools: [Python, HTML, vega-lite]
image: assets/pngs/pay.png
description: This is a final project!
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


# State of Pay: Unveiling Illinois Public Employee Compensation

## Dataset Overview

Visualizations are based on the state employee dataset from Illinois that contains employees who have been sworn in as law enforcement officers. The dataset includes columns such as agency, agency division, employee name, position title, period pay rate, and year-to-date (YTD) gross pay. According to Cornell University, state employees refer to individuals who are employed by the state and the services that they provide which are being financed by the United States/Federal agency. Period pay rate refers to the amount an employee is paid based on a specific time frame, for example, bi-weekly or monthly. While year to date is the amount of money the employee has gotten paid starting from January 1 to the most recent time the dataset has been updated. Each row then is an individual employee who works as a state employee in Illinois. In this dataset, there are 6 columns which were previously mentioned, and there are 104,000 rows. Overall, our dataset is tracking how much state employees are paid across their agency while still having a specific position title.

## Interactive Analysis: Position Title vs Pay Rate

<div class="alert alert-info" role="alert">
  <i class="fas fa-info-circle"></i> <strong>Note:</strong> Please select an agency from the dropdown menu, then click on a position title in the bar chart to see detailed salary information in the scatter plot below! Double click the position to back to overview in the scatter plot.
</div>

<vegachart schema-url="{{ site.baseurl }}/assets/json/employee_pay_analysis.json" style="width: 100%"></vegachart>

When looking at the "Position Title vs Pay Rate (Filtered by Agency, Top 20 Positions)" visualization, it creates a bar graph that changes when there is interactivity with the drop-down box. The drop-down box is located below the scatter plot, which is the second visualization under the name "Pay rate vs YTD (Selected Agency Highlighted)". You first have to interact with the drop-down box, where you have the ability to pick one agency to explore. One has to click on the drop-down box, and they will get a variety of options where they can select one that will change both graphs.

The first visualization is a bar chart, where the horizontal axis, known as the x-axis, refers to the different position titles with the agency that was picked in the drop-down box. For better readability, only the top 20 highest-paying positions within the selected agency are displayed. Meanwhile, the vertical axis, known as the y-axis, is the average pay rate. The average pay rate is calculated by adding up all period pay rate of the employees who have the same position title within the specific agency, and then that number is divided by the number of employees who have the same position title. The bar chart organizes the different position titles from the highest pay rates to the lowest pay rates. The positions that are located on the left have the highest average pay rate, meaning that they earn more money. In contrast to the positions on the right of the bar chart, they receive a lower amount of pay. Hence, as you move to the right, the average pay rate decreases per position title. In order to know more specifics regarding the average pay rate, you are also able to click on a specific bar in the chart and it will highlight that specific bar and provide the details regarding the agency, position title, and the specific average pay rate. Overall, the visualization shows the top 20 highest-paying position titles based on a specific agency and their average pay rate.

The Pay rate vs YTD Gross (Selected Agency Highlighted) is a scatter plot that requires you to select and click on a bar chart from the Position Title vs Pay Rate graph. After selecting a specific position title, the scatter plot will adjust and show data points in the scatter plot based on the individuals who are in that position title and it will show their specific period pay rate, as well as their year to date gross income. Overall, each dot represents an individual employee, and their position of the data shows their pay rate compared to their year to date earnings. The farther they are on the right, means that they get a higher pay per check. The higher up they are, means that they earned more money throughout this year. One also has the ability to not click on a particular bar if they choose to see the overall individual points of all the individuals within that specific agency.

## Contextual Visualizations

![Federal Workers Salary Distribution]({{ site.baseurl }}/assets/pngs/SR_25.01.07_federal-workers_6.png)

This image was produced by Pew Research Center in an article addressing questions the general population have regarding the impact of DOGE and President Trump's movement to shrinking the federal worker population. Although our analysis solely focuses on the federal employee pay in Illinois, our group found that this visualization assists in comparing a single state to the entire country. The primary source for graph was the Office of Personnel Management's FedScope data portal. This portal provides access to data on nearly all executive-branch employees. The main exception to this dataset are the U.S. Postal Service, congressional staffers, employees of the CIA and other intelligence agencies, and presidential appointees who require Senate confirmation. FedScope protects personal privacy by removing datapoints smaller than 12. Additionally, it removes location information of agencies in the FBI, Secret Service, DEA, the Bureau of Alcohol, Tobacco, Firearms and Explosives, and the U.S. Mint. Pew Research Center also grabbed data from civilian-employment data from the Bureau of Labor Statistics to compare the federal workforce with the national workforce as a whole. The Congressional Research Service also was relied on since they did a report on the federal civil service about how to define the different classifications of federal workers. From the above image, we see that about half of federal workers make a range of $50K-$109K a year. While only 3.1% of the federal workers making $200K or more.

![Federal Workers by State]({{ site.baseurl }}/assets/pngs/SR_25.01.07_federal-workers_3.png)

The same article provides another figure relevant to our analysis, in which it maps the presence of federal workers per state. Looking at Illinois specifically, we see that there is less than 1% of all nonfarm payroll employees that are federal civilian workers. Visually, it seems that a majority of the midwest lack presence of federal workers. Keeping this in mind as we analyze Illinois State federal workers pay can explain any discrepancies of position title and pay rate.

These visualizations were taken from Pew Research Center based on an article titled ["What the data says about federal workers"](https://www.pewresearch.org/short-reads/2025/01/07/what-the-data-says-about-federal-workers/).

## Comparative Analysis

There is also a contextual visualization that focuses on federal workers and shows the disparity regarding how much they earn within a year. As stated in the Pew research visualization, "50.8% of federal workers make $50,000 to $109,999 (Desilver 2025)". The visualization gives us an idea of how employees within the federal government get compensated. Connecting this visualization with the scatter plot of employee pay, it gives us insight into specific individuals who work as state employees. The scatter plot allows us to see whether or not individuals who work for the state are getting similar pay rates as those individuals who work in federal agencies. The federal workers' visualization focuses on displaying the percentage of employees are receiving such salary. Meanwhile, the scatter plot allows us to see the disparity of all the different individuals and their specific period pay rate as well as their year to date gross pay. Such visualization can help decide whether or not one should work for the state or for the federal.

The second visualization, "Where federal workers have the largest presence," shows the presence of federal workers within the United States and there is this misconception that most federal workers are being employed in the Washington DC area. However, this visualization shows that employees are scattered all across the United States with a scale showcasing what percentage of employees are located within a particular state. Within the map, the darker colors showcase a higher percentage of federal employees working in that state, while the circles show the number of employees working in that state. This visualization allows us to understand where federal workers are distributed within the United States. It is also important to highlight that there are federal workers that are not included in the visualization as there is "about 30,800 federal employees work overseas" (Desilver 2025). Provides us with a general understanding of where federal workers are being employed.

## References

Cornell Law School. (2025). Definition: State or local officer or employee from 5 USC § 1501(4). Legal Information Institute. Retrieved December 11, 2025, from [https://www.law.cornell.edu/definitions/uscode.php?height=800&def_id=5-USC-730423938-824090996&term_occur=999](https://www.law.cornell.edu/definitions/uscode.php?height=800&def_id=5-USC-730423938-824090996&term_occur=999)

Desilver, D. (2025, January 7). What the data says about federal workers. Retrieved December 10, 2025, from Pew Research Center website: [https://www.pewresearch.org/short-reads/2025/01/07/what-the-data-says-about-federal-workers/](https://www.pewresearch.org/short-reads/2025/01/07/what-the-data-says-about-federal-workers/)

DoIT EAS. (2024, September 24). State Employee Pay. Retrieved December 10, 2025, from Illinois.gov website: [https://data.illinois.gov/Government-and-Public-Employees/State-Employee-Pay/iu6r-a89d/about_data](https://data.illinois.gov/Government-and-Public-Employees/State-Employee-Pay/iu6r-a89d/about_data)

<div class="left">
{% include elements/button.html link="https://github.com/UIUC-iSchool-DataViz/is445_data/raw/main/licenses_fall2022.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/yfxuyeah/yfxuyeah.github.io/blob/main/python_notebooks/licenses_fall2022_analysis.ipynb" text="The Analysis" %}
</div>