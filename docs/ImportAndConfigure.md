# Import and configure your postman collection

## How to import a postman collection

Click on the import menu entry of postman, 

![import a collection](img/collection-import.png)


Select "Import from link" and specify the URL of the collection to import.

![import a collection](img/collection-import-from-link.png)



## Configure your execution environement

Postman lets you define [environment variables](https://www.getpostman.com/docs/environments) to easilly abstract your execution contexts.

This is where we'll specify the token used to access the Cisco Spark API.

> Tip: 
> create [several environments to switch](https://www.getpostman.com/docs/test_multi_environments) from one Spark account to another.
> As for instance, to jump back and forth from your personal account to one or several of your bot accounts.

To create a new environment, click on the ![](img/environment-create-icon.png) icon in the upper right corner, and select "Manage environments".

![](img/environment-create.png)


In the "Manage environments" dialog, add the "spark_token" variable, and paste your Spark personal access token (without the Bearer prefix).
Note that you can retrieve this token from the [Spark for developers](https://developer.ciscospark.com) portal, by clicking on your avatar, or by copy pasting from the resources documentation when in test mode.

![](img/environment-configure.png)







