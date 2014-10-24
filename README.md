# API-standards
This repository collects research on API standards, particularly those focused on Open Data / Open Government. 


## Data Formats (in descending order of importance)
* JSON
* CSV
* XML
* HTML
* JSONP

# Ambiguity in Standards
There are some areas where standards are not specific. As we settle on which convention we wish to use, we must decide:
* Metadata location - in a separate file, or in one JSON object as a peer to the dataset?
* Naming conventions - dataset-level metadata vs. column definition metadata etc.

## 

## Conflicting Standards
=============
The various best practices, standards, and other materials contain some conflicting information. 

* **camelCase vs. snake_case for JSON keys:** [18f's API standards](https://github.com/18F/api-standards) specify snake (or "underscore") case. [Project Open Data's Common Core Metadata Schema](http://project-open-data.github.io/schema/) specifies camelCase for JSON keys in metadata.

## Standards Source Material
| Source | URL |
| --- | --- |
| 18f / API Standards | https://github.com/18F/api-standards |
| Project Open Data / Common Core Metadata Schema | http://project-open-data.github.io/schema/ |
| 18f / API all the X | https://github.com/18f/API-All-the-X |
|  |  |
| Google / Dataset Publishing Language (DSPL) | https://developers.google.com/public-data/ |

## Reference APIs
| Source | URL |
| --- | --- |
| CFPB / HMDA | http://cfpb.github.io/api/hmda/ |

## API Platforms
* [CFPB Qu](http://cfpb.github.io/qu/)
* [api.data.gov](http://api.data.gov/about/)
* [CKAN](http://ckan.org/)
