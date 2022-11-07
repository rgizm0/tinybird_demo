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

