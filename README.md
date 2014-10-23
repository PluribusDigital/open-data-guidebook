# API-standards
This repository collects research on API standards, particularly those focused on Open Data / Open Government. 


# Ambiguity in Standards
There are some areas where starndards are not specific. As we settle on which convention we wish to use, we must decide:
* Metadata location - in a separate file, or in one JSON object as a peer to the dataset?
* Naming conventions - dataset-level metadata vs. column definition metadata etc.

## 

## Conflicting Standards
=============
The various best practices, standards, and other materials contain some conflicting information. 

* **camelCase vs. snake_case for JSON keys:** [18f's API standards](https://github.com/18F/api-standards) specify snake (or "underscore") case. [Project Open Data's Common Core Metadata Schema](http://project-open-data.github.io/schema/) specifies camelCase for JSON keys in metadata.
