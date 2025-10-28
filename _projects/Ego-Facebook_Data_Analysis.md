---
name: Ego-Facebook Data Analysis
tools: [Python, HTML, vega-lite]
image: assets/pngs/cars.png
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

Before visualization, the data was transformed using Python by grouping the original dataset by 'City', aggregating the size of each group into a 'counts' column, sorting this new DataFrame by 'counts' in descending order, and finally, slicing the DataFrame to retain only the top 10 rows.


## Search The Data & Methods

Below is where we can put some links to both the data and the analysis code as buttons:

```
<div class="left">
{% include elements/button.html link="https://github.com/vega/vega/blob/main/docs/data/cars.json" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://blog.4dcu.be/programming/2021/05/03/Interactive-Visualizations.html" text="The Analysis" %}
</div>
```

<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://github.com/UIUC-iSchool-DataViz/is445_data/raw/main/licenses_fall2022.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/jnaiman/online_cv_public/blob/main/python_notebooks/test_generate_plots.ipynb" text="The Analysis" %}
</div>

# Ego-Facebook Data Analysis

We conduct a general analysis on ego-facebook dataset. 

