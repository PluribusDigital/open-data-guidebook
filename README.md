# Open Data Guidebook
The concept of Open Data and Open Government have the potential to spur innovation, or at least make it easier to get information. This document intends to provide an opinionated guide on how to get started. The hope is to capture best practices and conventions. 

## Problems This Guide Solves
In developing a data sharing program, there are dozens of small decisions to be made. There are also a lack of strong conventions for government agencies in the specifics of how to share data. This guide offers a set of baseline decisions that are made for you, that are best practice or very close. 

## Problems This Guide *Does Not* Solve
This is not a thoughtful consideration of your agency's specific needs. There are any number of reasons to go against the conventions laid out here.

## Assumptions
These guidelines work well for the majority of datasets. This is not meant to solve the most complex cases (i.e. Census should probably look elsewhere for their core data sets and APIs).

# The Guidelines

In approximate order of priority, the guidelines are as follows and explained below. Generally, the earlier items are higher value (more important, less effort). Many agencies may stop at item 3, and that can be perfectly valid.

1. Publish bulk data 
2. Provide a /data.json index file 
3. Publish dataset definitions/dictionaries
4. Create APIs
5. Make data available in multiple formats
6. Document APIs and datasets in a /developer page
7. Create data browsing applications
8. Market the datasets
9. Create a github repo for each API
10. Use API keys 

## 1. Publish bulk data 
If you do nothing else, make data available. 
* If you truly must, publish the data in HTML or PDF format. Sharing anything beats sharing nothing.
* Please also publish the same dataset as CSV. This format is friendly for computers to read, so developers can build applications on top of the data. Also, CSV opens automatically in popular software like Microsoft Excel.
* If someone wants to do something fancy (filter, sort, etc.), they can pull the data into a spreadsheet.
* Hopefully the data is clean and accurate.

This is simple, and is published as static web content. No coding necessary. You can use whatever current technology the agency has, such as a content management system software (e.g. Drupal).

## 2. Provide a /data.json index file 
At the root of your web domain, provide a /data.json file (e.g. http://www.justice.gov/data.json). 
* This allows your datasets to be accessible in the [data.gov directory](https://www.data.gov/about#collected)
* Update /data.json when datasets are added/changed.
* See also: [getting your data listed on data.gov], including information on the json format (https://www.digitalgov.gov/resources/how-to-get-your-open-data-on-data-gov/#non-federal-data).

Note: creating a json file seems intimidating to a non-developer, but it is pretty simple once you get the hang of it. You can use any text editor. The free [Atom editor](https://atom.io/) makes it easier still, and you could even use an online editor such as [JSON Editor Online (no endorsement/warranty)](http://jsoneditoronline.org/). *You can do it!*

## 3. Publish dataset definitions/dictionaries
Describe the data elements (aka columns) contained in each dataset. 
* At a minimum, provide this as static web content, available along with the links to the raw data.
* You may alternatively provide a dictionary in CSV format (column title, definition, etc.)

*Note: this is potentially superceded if you create more robust developer/API documentation.*

## 4. Create APIs
Any large dataset becomes difficult to consume as a bulk data file. (However, please do make even the big datasets available as bulk data.) An API is a software application that allows the data to be queried, generally by another computer/application. 

API design is a big subtopic, and is broken out into a separate page: [API Design Guide](APIDESIGN.md).

## 5. Make data available in multiple formats

## 6. Document APIs and datasets in a /developer page

## 7. Create data browsing applications

## 8. Market the datasets

## 9. Create a github repo for each API

## 10. Use API keys 


----------

# Appendix


# Surrounding API Recommendations
* Contact email
* Github issue tracker to capture Q&A
* Documentation page (see also http://gsa.github.io/Open-Data-Collaboration-Sandbox/ for forkable github pages examples)
* Developer blog
* /developer page

### API Best Practices
* Version the API

# Organization-level Data Metadata

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
| JSONAPI Spec | http://jsonapi.org/ | 
| GRAPHQL Spec | http://graphql.org/ |

## Reference APIs
| Source | URL |
| --- | --- |
| CFPB / HMDA | http://cfpb.github.io/api/hmda/ |

## API Platforms
* [CFPB Qu](http://cfpb.github.io/qu/)
* [api.data.gov](http://api.data.gov/about/)
* [CKAN](http://ckan.org/)
* [DKAN](http://getdkan.com/)
* [Socrata](http://socrata.com/) - commercial
 
## Additional Tools
* [Swagger](http://swagger.io/) for interactive API documentation

# Reference Examples of JSON Response Formats
http://www.justice.gov/api/v1/blog_entries.json?fields=title,created&pagesize=10
{"metadata":{"responseInfo":{"status":200,"developerMessage":"OK"},"resultset":{"count":1581,"pagesize":10,"page":0},"executionTime":0.080682992935181},"results":[{"created":"1317655920","title":"Message from Director Carbon: October 2011"},{"created":"1315064102","title":"Message from Director Carbon: September 2011"},{"created":"1312212952","title":"Message from Director Carbon: August 2011"},{"created":"1309534625","title":"Message from Director Carbon: July 2011"},{"created":"1306942702","title":"Message from Director Carbon: June 2011"},{"created":"1304350789","title":"Message from Director Carbon: May 2011"},{"created":"1304091657","title":"Message from Director Carbon: April 2011 (2 of 2)"},{"created":"1301931992","title":"Message from Director Carbon: April 2011 (1 of 2)"},{"created":"1299604240","title":"Message from Director Carbon: March 2011"},{"created":"1296580299","title":"Message from Director Carbon: February 2011"}]}
