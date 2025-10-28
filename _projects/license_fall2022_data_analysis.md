---
name: License Fall2022 Data Analysis
tools: [Python, HTML, vega-lite]
image: assets/pngs/license.png
description: This is a homework project!
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


# License_2022fall data analysis

## Geographic analysis


<vegachart schema-url="{{ site.baseurl }}/assets/json/geographic.json" style="width: 100%"></vegachart>

This bar chart visualizes the "Top 10 Cities by Number of License Holders in Fall 2022, IL," plotting the nominal 'City' category on the x-axis against the quantitative 'counts' on the y-axis. 

Key design choices include using mark_bar() for easy comparison, sorting the x-axis by the y-value ('counts') in descending order, and setting x-axis labels horizontally (labelAngle=0) for readability. A logarithmic scale (type='log') was applied to the y-axis where the top city's count is orders of magnitude larger than the others. A tooltip was also added for interactivity. 

ColorMap was unnecessary because it simply compares the number of license holder in a bar chart.

Before visualization, the data was transformed using Python by grouping the original dataset by 'City', aggregating the size of each group into a 'counts' column, sorting this new DataFrame by 'counts' in descending order, and finally, slicing the DataFrame to retain only the top 10 rows.


## Disciplinary Analysis(interactive)

<div class="alert alert-info" role="alert">
  <i class="fas fa-info-circle"></i> <strong>Note:</strong> Please click the bar in the left chart!
</div>



<vegachart schema-url="{{ site.baseurl }}/assets/json/discipline.json" style="width: 100%"></vegachart>

This visualization provides an interactive dashboard for exploring professional license disciplinary actions, featuring two linked bar charts. The left chart presents an overview of violation counts by 'License Type', while the right chart details the specific 'Top 5 Discipline Reason'.

The design encodes 'License Type' and 'Discipline Reason' as nominal data on the x-axes, with record counts as quantitative data on the y-axes. A colormap was unnecessary; instead, the chart uses conditional fillOpacity to encode the selection status, causing unselected bars to fade. A key data transformation is the symlog scale on the left chart's y-axis, which properly visualizes the large variance in counts across different professions.

Interactivity is central to this visual. A selection_point on the left chart drives the analysis. When a user clicks a 'License Type', this selection highlights the chosen bar and, most importantly, applies a transform_filter to the right chart. This action instantly filters the detail view to show only the reasons relevant to the selected profession.

<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://github.com/UIUC-iSchool-DataViz/is445_data/raw/main/licenses_fall2022.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/yfxuyeah/yfxuyeah.github.io/blob/main/python_notebooks/licenses_fall2022_analysis.ipynb" text="The Analysis" %}
</div>


