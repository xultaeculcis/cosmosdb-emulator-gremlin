# cosmosdb-emulator-gremlin
Azure Cosmos DB is Microsoft's globally distributed multi-model database service. You can quickly create and query document, table, key-value, and graph databases, all of which benefit from the global distribution and horizontal scale capabilities at the core of Azure Cosmos DB. 

Cosmos Emulator now supports Gremlin API (since version 2.1.4), however no one bothered to mention how to run it and how to connect to it. The Cosmos DB Emulator documentation page also seems to be out of date, so I decided to figure it out on my own.

This quick start sample program shows how to get started with the Graph (Gremlin) API for Azure Cosmos DB using the open-source connector Gremlin.Net and Cosmos DB Emulator.

## IMPORTANT
This repo is no longer maintained. Cosmos DB Emulator documentation now clearly shows how to use Graph API. Please follow instructions on [Install and use the Azure Cosmos DB Emulator for local development and testing - Gremlin API](https://docs.microsoft.com/en-us/azure/cosmos-db/local-emulator?tabs=ssl-netstd21#gremlin-api).

## Getting started
1. Clone this repository.

2. Open the GremlinNetSample.sln solution and restore the packages. 
3. Go to your Cosmos DB Emulator install location and open PowerShell window in that location. Default install path is `C:\Program Files\Azure Cosmos DB Emulator`
4. Gremlin Endpoint is not enabled by default. To enable it run Cosmos DB Emulator from CMD/PowerShell using following command: 
```powershell
.\CosmosDB.Emulator.exe /EnableGremlinEndpoint
```
 5. Gremlin Endpoint will be opened on port `8901` by default. If you want to change that port run Emulator wiht follwing command:
 
 ```powershell
.\CosmosDB.Emulator.exe /EnableGremlinEndpoint /GremlinPort=<port_number>
```
6. Endpoints in the sample are preconfigured to run with the Emulator. You don't have to change anything apart for db, graph and partition key property names.
7. Build and Run the project.

## More information

- [Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/introduction)
- [Gremlin API](https://docs.microsoft.com/en-us/azure/cosmos-db/graph-introduction)
- [Apache Tinkerpop](https://tinkerpop.apache.org/)
