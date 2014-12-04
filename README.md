# API-standards
This repository collects research on API standards, particularly those focused on Open Data / Open Government. 


## Data Formats (in descending order of importance)
* JSON
* CSV
* XML
* HTML
* JSONP

## Common Best Practices
* Entire datasets first (a query API is great, but at a minimum, put out the entire raw dataset)

# Surrounding API Recommendations
* Contact email
* Github issue tracker to capture Q&A
* Documentation page (see also http://gsa.github.io/Open-Data-Collaboration-Sandbox/ for forkable github pages examples)
* Developer blog
* /developer page

### API Best Practices
* Version the API

# Organization-level Data Metadata
Some organizations have a list of datasets as an API (e.g. http://www.justice.gov/data.json)

# Ambiguity in Standards
There are some areas where standards are not specific. As we settle on which convention we wish to use, we must decide:
* Metadata location - in a separate file, or in one JSON object as a peer to the dataset?
* Naming conventions - dataset-level metadata vs. column definition metadata etc.
* Versioning - put version in API url? where? http://api.agency.gov/resource/v1 vs. http://api.agency.gov/v1/resource

## Conflicting Standards
The various best practices, standards, and other materials contain some conflicting information. 
* **camelCase vs. snake_case for JSON keys:** [18f's API standards](https://github.com/18F/api-standards) specify snake (or "underscore") case. [Project Open Data's Common Core Metadata Schema](http://project-open-data.github.io/schema/) specifies camelCase for JSON keys in metadata.

## Standards Source Material
| Source | URL |
| --- | --- |
| 18f / API Standards | https://github.com/18F/api-standards |
| Project Open Data / Common Core Metadata Schema | http://project-open-data.github.io/schema/ |
| 18f / API all the X | https://github.com/18f/API-All-the-X |
| CFPB Qu Data Formats | http://cfpb.github.io/qu/data_formats.html |
| Google / Dataset Publishing Language (DSPL) | https://developers.google.com/public-data/ |
| White House API Standards | https://github.com/WhiteHouse/api-standards |

## Reference APIs
| Source | URL |
| --- | --- |
| CFPB / HMDA | http://cfpb.github.io/api/hmda/ |

## API Platforms
* [CFPB Qu](http://cfpb.github.io/qu/)
* [api.data.gov](http://api.data.gov/about/)
* [CKAN](http://ckan.org/)
* [Socrata](http://socrata.com/) - commercial
 
## Additional Tools
* [Swagger](http://swagger.io/) for API documentation

# Reference Examples of JSON Response Formats
http://www.justice.gov/api/v1/blog_entries.json?fields=title,created&pagesize=10
{"metadata":{"responseInfo":{"status":200,"developerMessage":"OK"},"resultset":{"count":1581,"pagesize":10,"page":0},"executionTime":0.080682992935181},"results":[{"created":"1317655920","title":"Message from Director Carbon: October 2011"},{"created":"1315064102","title":"Message from Director Carbon: September 2011"},{"created":"1312212952","title":"Message from Director Carbon: August 2011"},{"created":"1309534625","title":"Message from Director Carbon: July 2011"},{"created":"1306942702","title":"Message from Director Carbon: June 2011"},{"created":"1304350789","title":"Message from Director Carbon: May 2011"},{"created":"1304091657","title":"Message from Director Carbon: April 2011 (2 of 2)"},{"created":"1301931992","title":"Message from Director Carbon: April 2011 (1 of 2)"},{"created":"1299604240","title":"Message from Director Carbon: March 2011"},{"created":"1296580299","title":"Message from Director Carbon: February 2011"}]}
