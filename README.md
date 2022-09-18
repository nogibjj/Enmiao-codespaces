# IDS706 Project1 Enmiao Feng

[![Python application test with Github Actions](https://github.com/nogibjj/ids-706-project-1-chang/actions/workflows/main.yml/badge.svg)](https://github.com/nogibjj/enmiao-codespaces/actions/workflows/main.yml)

## Overview
This project build a command-line tool that talks to a big data system. We us Azure Databricks to operate datas. To communicate with the database on Databricks, this project uses the Python Databricks library. The users can use CLI to query the DataBase.

## Databricks and Microsoft Azure
The database of this project is kept on Databricks and Databricks is run on Microsoft Azure. Databricks is based on Apache Spark, so we can leverage its parallel nature when doing queries.

We need the following four secrests to connect and communicate with our Databrick cluster.
- ```DATABRICKS_HOST```
- ```DATABRICKS_HTTP_PATH```
- ```DATABRICKS_SERVER_HOSTNAME```
- ```DATABRICKS_TOKEN```

## Test connection
We can use ```databricks-cli``` to test connection and print clusters information. Run the following CLI command.

```
databricks clusters list --output JSON | jq
```

## CLI interface
This project uses ```click``` to build a CLI interface from which users can execute queries. Use the following command.

```
./query.py cli-query
```

or

```
./query.py cli-query <--query QUERYTEXT>
