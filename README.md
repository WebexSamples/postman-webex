# Postman collections for Cisco Spark

This repo's goal is to regroup community Postman collections for the Cisco Spark API v1, as documented on [Spark for Developers](https://developer.ciscospark.com/quick-reference.html).

**We welcome enhancements to the collections below, as well as contributions of collections that proved to be handy for you over time. 
Please submit a pull request. 
Thank you!** 


## all-resources-scripted

Introduced at Cisco Live Vegas in July 2016, the collection was made available through [bit.ly](bit.ly/POSTMAN-SPARK-API).
It is now maintained in this repository.

The collection illustrates the full set of Spark API resources, with direct link to the official API documentation.

![all resources](img/scripted-collection-all-resources.png)

The collection is scripted so that you can run in a row all REST call for a resource.
Concretely, the identifier of any resource created is retreived automatically and injected into the next REST query.
Moreover, all newly created Spark resources are freed at the end of each resource scenario.

![messages](img/scripted-collection-messages.png)

After importing the collection into postman, [create a new environment and add the spark_token variable](HowToCreatePostmanEnvironments.md).

Select your new postman environment.

You're good: the collection can now be run straight away.


