# Postman collections for Cisco Spark

This repo's goal is to regroup community Postman collections for the Cisco Spark API v1, as documented on [Spark for Developers](https://developer.ciscospark.com/quick-reference.html).

Quick guides to take full benefits of these collections, :
- [import and configure](docs/ImportAndConfigure.md) a collection 
- [generate code](docs/GenerateCode.md) for your favorite language
- [run collections](docs/RunCollectionsCI-CD.md) as part of your CI/CD process   

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

After [importing the collection](ImportAndConfigure.md), select one of your postman environment, and the collection can now be run straight away.
For example, go to the Rooms directory entry, and run the requests in the displayed order.

![messages](docs/img/scripted-collection-messages.png)



