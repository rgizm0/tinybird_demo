# tinybird_demo
This is a demo for Tinybird.

This demo includes:

## Datasources
Real UK Police crime data (puplic dataset)
- reported street criime
- reported street crime outcomes

Tinybird Pipes
- police outcomes clean
- police street crime crlean
- crime summary
- outcome summary
- closed crime outcomes

# Getting started
Requirements
The following python packages are required:

tinybird-cli

# Getting the data loaded to Tinybird
Use the [Tinybird cli](https://www.tinybird.co/docs/cli.html) to deploy this project.

```bash
tb push --push-deps
```
Data can now be loaded to the newly created tables
```bash
tb push datasources/police_street.datasource
tb push datasources/police_outcomes.datasource
```
# The dataflow
This dataflow demonstrates the 3 typical steps of data analysis
1. Data cleaning (here we remove rows will null data)
2. Data preparation (creating summary views of reported and solved crime)
3. Data mining (joining datasets to identify data with additional meaning)

# Endpoints
API endpoints have been defined for ech of the pipelines. Most of the endpoints have optional parameters tht would allow filters to be applied to the api call. As they are optional, simply calling the api with no parameters will return the full resultset.

# The benefits of using Tinybird for this workflow
Tinybird allows rapid development of the dataflow & pipeines. By using notebook style of development it is easy to break down complex queries and transformations into maller easier queries. As each pipeline can be published with its own API external tools and software suites can easily interact with Tinybird without requiring any additional software or drivers to be installed and maintained. For devops, haviing a easy to use GUI with graphical metrics for datasets and pipelines make it easy to detect performance bottlenecks and respond proactively. 
