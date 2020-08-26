# Postman for Webex Messaging and Admin APIs

This repo gathers Postman collections for **[Webex Messaging and Admin APIs](https://developer.webex.com/quick-reference.html)**.
- [Webex Messaging API](#webex-messaging-api): Messages, Rooms, Teams, People, Webhooks, AttachmentActions... all Webex resources accessible from an access token, with no admin priviledges.
- [Webex Admin API](#webex-admin-api): Organizations, People creation and updates, Roles, Licenses, Events, Devices, Places and xAPI. These admin related features are accessible only with an access token with admin priviledges.
- [Webex Cards](#webex-cards): Messages (with Card attachments), AttachmentActions and Card examples.

Looking for other postman collections, check:
- [postman-xapi](https://github.com/CiscoDevNet/postman-xapi) if looking for collections for **Webex Devices Cloud  API**.
- [postman-webex-calling](https://github.com/webex/postman-webex-calling) if looking for collections for **Webex Calling API**.
- [postman-webex-meeting](https://github.com/webex/postman-webex-meetings) if looking for collections for **Webex Meeting REST API**.

If you're new to Postman, you're only a few steps away from getting the full benefits of the collections:
1. [import and configure](docs/ImportAndConfigure.md) a collection 
2. [generate code](docs/GenerateCode.md) for your favorite language
3. [run collections as part of your CI/CD process](https://www.getpostman.com/docs/newman_intro) via the newman command
4. [publish documentation via documenter](https://www.getpostman.com/docs/creating_documentation).

**We welcome pull requests for enhancements of existing collections, as well as contributions of collections that proved to be handy for you. 
When submitting a new collection, please ensure it leverages a {{access_token}} variable to ease environments sharing among collections. Thank you!** 


## [Webex Messaging API](https://raw.githubusercontent.com/CiscoDevNet/postman-webex/master/all-resources-scripted.json)

[![Run in Postman](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/1f5e101d8290a5303c90)

The collection regroups public resources for the Webex Messaging REST API, with direct links to the official API documentation.
The collection a simple user account, no need admin priviledges are required.

![public resources](docs/img/scripted-collection-all-resources.png)

Worth mentionning that the collection is scripted so that you can run REST calls in a row for any given resource:
- as you run REST queries from top to bottom, newly created resource identifiers are automatically retreived and injected into your postman environment as temporary variables,
- so that the next REST query will look from the postman environment, and execute in the context of the previous query. For example, you'll add a message into the space you just created in the previous step. 
- at the end of each scenario (embedded in individual collection folders), we've added requests to free newly created resources so that you'll end up in the same state as before running the queries in postman.

Enough talk, let's practice:
- [import the all-resources-scripted collection](docs/ImportAndConfigure.md), 
- create or select a postman environment that contains a {{access_token}} variable, 
- now, you're ready to invoke the API: for example, go to the Messages folder, and run the requests from top to bottom.

![memberships](docs/img/scripted-collection-memberships.png)

Now, what about generating some code for your favorite language ?

Take the [Generate Code Guide](docs/GenerateCode.md) and have this Node.js code snippet automatically generated for the API Resource "List spaces":

![generate code](docs/img/generate-nodejs-request-no-postman-header.png)

Note that the collection is also rendered in HTML for [quick browsing via Postman Documenter](https://documenter.getpostman.com/view/30210/71CYsEp).


## [Webex Cards](https://raw.githubusercontent.com/CiscoDevNet/postman-webex/master/cards-scripted.json)

[![Run in Postman](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/0b1f13e0bb8cabd8b84c)

This collection lets you experiment [Webex Cards and Buttons](https://developer.webex.com/docs/api/guides/cards).

You'll need to create an environment with the following variables:
   - `access_token`: a Webex API access token
   - `bot_token`: the token of a Webex Bot account

![Webex Cards](docs/img/cards-scripted-collection.png)

Note that the collection is also rendered in HTML for [quick browsing via Postman Documenter](https://documenter.getpostman.com/view/30210/SVfTPTQ4).


## [Webex Admin API](https://raw.githubusercontent.com/CiscoDevNet/postman-webex/master/admin-scripted.json)

[![Run in Postman](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/0aa22af74405f82086d4)

The collection illustrates the REST API **Administration Resources**, with direct link to the [Admin API documentation](https://developer.webex.com/docs/api/guides/admin-api).

Note that the collection is also rendered in HTML for [quick browsing via Postman Documenter](https://documenter.getpostman.com/view/30210/2PMC7h).

![admin-api](docs/img/admin-scripted-collection.png)

The People folder is populated with pre-request and post-request scripts in order to ease the creation of random accounts.

![admin-api](docs/img/admin-scripted-collection-people.png) 

