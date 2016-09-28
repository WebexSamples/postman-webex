# Postman collections for Cisco Spark

This repo's goal is to regroup community Postman collections for the Cisco Spark API v1, as documented on [Spark for Developers](https://developer.ciscospark.com/quick-reference.html).

Quick guides to take full benefits of these collections, :
- [import and configure](docs/ImportAndConfigure.md) a collection 
- [generate code](docs/GenerateCode.md) for your favorite language

Note that the postman suite lets you [run collections as part of your CI/CD process](https://www.getpostman.com/docs/newman_intro) via the newman command, and can also help you [publish documentation via documenter](https://www.getpostman.com/docs/creating_documentation).    

**We welcome enhancements to the collections below, as well as contributions of collections that proved to be handy for you over time. 
Please submit a pull request. 
Thank you!** 


## all-resources-scripted

Introduced at Cisco Live Vegas in July 2016, the collection was made available through [bit.ly](bit.ly/POSTMAN-SPARK-API).
It is now maintained in this repository.

The collection illustrates the full set of Spark API resources, with direct link to the official API documentation.

![all resources](docs/img/scripted-collection-all-resources.png)

The collection is scripted so that you can run REST calls in a row :
- newly created resource identifiers are automatically retreived and injected into the next REST query,
- all newly created Spark resources are freed at the end of each scenario.

After [importing the collection](ImportAndConfigure.md), select a postman environment, and you're ready to invoke the Spark API.

For example, go to the Rooms directory entry, and run the requests in the displayed order.

![messages](docs/img/scripted-collection-messages.png)



