---
layout: default
title: Filters
parent: Dashboard
grand_parent: LASER How To
nav_order: 6
---

# How to use the Filters Pane

The Filters pane can be enabled by clicking on show or hide option on the right side of the report. Unless configured differently, all Power BI reports by default have the Filter pane available.

![Filter Show and Hide](../../../images/dashboard/dashboard_filters_show_hide.png)

There are different types of filters available;
- Report Level Filters
- Page Level filters
- Visual Level Filters

In this Report, there are no report level filters applied. Page level filters are available for the Landing Page and User Information page. Visual level filters are available on the VM usage, Project costs, Cost and budget and Resource cost pages.

This is to allow you to filter the quantity of data displayed on a particular page. 

To enabled visual level filters you need to select a single visual. Page level filters are available automatically.

For example, when there is a use case where a user wants to see the Top 10 resources by cost rather than the default Top 5 resources. Then the user can Show Filters, click on a visual and then update the first element in the filter to be 10 instead of 5 and click ‘Apply filer’, see screenshots below.

![Applying Filter 1](../../../images/dashboard/dashboard_filters_apply_1.png)
![Applying Filter 2](../../../images/dashboard/dashboard_filters_apply_2.png)
![Applying Filter 3](../../../images/dashboard/dashboard_filters_apply_3.png)

## Cross filtering in Power BI

By default Cross filtering is enabled for all visuals in Power BI. If you select a data point on one of the visuals, all of the other visuals on the page that contain that data change based on that selection.
[Understand how visuals interact in a report - Power BI | Microsoft Docs](https://docs.microsoft.com/en-us/power-bi/consumer/end-user-interactions)
For example, by default a page may look like below, displaying a number of projects a user may have access to.
 
When a specific project is selected, the rest of the visuals change to reflect that selection.

![Default Filter](../../../images/dashboard/dashboard_filters_cross_default.png)

Now the visuals inside the yellow box and the key metrics above are cross filtered based on the selection.

![Selected Filter](../../../images/dashboard/dashboard_filters_cross_specific.png)
