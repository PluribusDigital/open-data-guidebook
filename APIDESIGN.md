
# API Design Guide
This is a section of the Open Data Guidebook, broken out into its own page.

## Platform Strategy
There are many options to create APIs. Custom applications and off-the-shelf platforms are both viable. If you use a pre-built platform, then some of the design options are constrained, so just go with those.

## Data Formats 
The default choice is to make data available in JSON and CSV both. Most platforms make it fairly easy to serve data in multiple formats.

In descending order of importance, the primary formats to worry about are:
* CSV 
* JSON 
* XML
* HTML
* JSONP

*Note 1: JSON is better for applications to consume, CSV is better for humans.*

*Note 2: Some datasets cannot readily be represented in a "flat" form such as CSV.*

*Note 3: This doesn't include specialized formats such as GIS.*
