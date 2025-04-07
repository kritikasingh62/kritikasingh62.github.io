---
layout: default
title: Homework 5
---

## Visualization 1: UFO Sightings by Year and Shape
### What it shows:
This first visualization is a stacked bar chart showing the count of UFO sightings grouped by year and categorized by the reported shape of the UFO. The chart clearly communicates trends over time and gives a categorical breakdown to observe whether specific shapes became more commonly reported in certain periods. For example, we can see a spike in sightings in the late 1990s and 2000s, with a diverse distribution of shapes such as "light", "triangle", and "disk".

In terms of design choices, the x-axis encodes the year as an ordinal variable, while the y-axis encodes the count of sightings as a quantitative variable. The shape of the UFO is encoded using a color scheme, where each shape category has its own distinct color. The stacked bar design helps compare both overall volume of sightings over time and relative frequency of shapes within each year. I used a legend with two columns to improve readability and make it easier to distinguish among the many shapes.

For data transformation, I first parsed the datetime column into a timestamp and extracted the year component. I also removed any records where the shape was missing or marked as "unknown", since including these would skew the analysis with incomplete or ambiguous data.

This chart is not reused from Homework #5. Although the concept of grouping by year was explored in Homework #5, that previous version did not include categorical color encoding or a multi-shape breakdown. This stacked bar chart introduces a more detailed multivariate analysis and improves clarity through better axis labels and visual grouping.

### Design Choices:
- **X-axis**: [explanation]
- **Y-axis**: [explanation]
- **Color encoding**: [explanation]

The color scheme used is [name of scheme], chosen because ...

[Optional] Transformations: Grouping by [field], filtering for [condition], etc.

### Interactivity:
This chart allows the user to [explanation of interactive features like hover, zoom, etc.].

---

## Visualization 2:  Interactive Sightings Over Time by Shape
### What it shows:
The second visualization shows a line chart of UFO sightings over time, specifically by month, and incorporates interactivity through a dropdown filter. Users can select a specific shape of UFO (e.g., "light", "disk", "triangle") and the chart dynamically updates to show how sightings of that shape have trended over time. This makes it possible to explore whether certain shapes were reported more frequently in specific eras or if their popularity fluctuated.

The encodings include month on the x-axis (as a temporal variable), and the count of sightings on the y-axis (as a quantitative measure). The line itself is colored a consistent blue (#1f77b4) to keep the focus on the shape selection and temporal trend rather than categorical comparisons.

The main data transformation involved converting the datetime into a month value using .dt.to_period("M").dt.to_timestamp(), allowing grouping by month while preserving temporal granularity. Like the first plot, I also filtered out rows with missing or unknown shapes.

This plot is new and not reused from Homework #5. While Homework #5 used time-series data, it did not include interactivity or allow filtering by shape. This updated version adds richer exploration capabilities through the use of Altair’s selection_single and binding_select.

### Design Choices:
- **X-axis**: [explanation]
- **Y-axis**: [explanation]
- **Color encoding**: [explanation]

The color scheme is [name of scheme], chosen to ...

[Optional] Transformations: [details]

### Interactivity:
I implemented interactivity using a dropdown menu that allows the user to select a UFO shape and see a corresponding time-series of sightings. This adds a layer of exploration and personalization to the chart — rather than overwhelming the viewer with 20+ shape lines, they can drill into the one that interests them. It also improves readability and interpretability by reducing visual clutter while still preserving full access to the underlying data.

---

### Links:
- [The Data](https://github.com/UIUC-iSchool-DataViz/is445_data/raw/main/ufo-scrubbed-geocoded-time-standardized-00.csv)
- [The Analysis](https://github.com/kritikasingh62/HW5.1/blob/master/HW5.1.ipynb)