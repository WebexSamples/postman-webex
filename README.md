# Postman collections for Cisco Spark

This repo's goal is to regroup community Postman collections for the Cisco Spark API v1, as documented on [Spark for Developers](https://developer.ciscospark.com/quick-reference.html).

Get full benefits of the collections in this repo in 2 steps:

1. [import and configure](docs/ImportAndConfigure.md) a collection 
2. [generate code](docs/GenerateCode.md) for your favorite language

Note that the postman suite lets you [run collections as part of your CI/CD process](https://www.getpostman.com/docs/newman_intro) via the newman command, and can also help you [publish documentation via documenter](https://www.getpostman.com/docs/creating_documentation).    

**We welcome pull request for enhancements of the existing collections, as well as contributions of collections that proved to be handy for you over time. 
When submitting a new collection, please ensure it leverages a {{spark_token}} variable to ease setup among collections.  
Thank you!** 


## [all-resources-scripted](https://raw.githubusercontent.com/CiscoDevNet/postman-ciscospark/master/all-resources-scripted.json)

Introduced at Cisco Live Vegas in July 2016, this collection was originally made available through [bit.ly](bit.ly/POSTMAN-SPARK-API).
It is now maintained in this repository.

The collection illustrates the full set of Spark API resources, with direct link to the official API documentation.

![all resources](docs/img/scripted-collection-all-resources.png)

Worth mentionning that the collection is scripted so that you can run REST calls in a row for any given resource:
- as you run REST queries from top to bottom, newly created resource identifiers are automatically retreived and injected into your postman environment as temporary variable,
- so that the next REST query will look from the postman environment, and execute in the context of the previous query. For example, you'll add a message into the room you just created in the previous step. 
- at the end of each scenario, we've added one or several requests to free newly created Spark resources so that you'll end up in the same state as before running the set of queries.

Enough talk, let's practice:
- [import the all-resources-scripted collection](docs/ImportAndConfigure.md), 
- create or select a postman environment that contains a {{spark_token}} variable, 
- now, you're ready to invoke the Spark API,
- for example, go to the Messages folder, and run the requests from top to bottom.

![messages](docs/img/scripted-collection-messages.png)
