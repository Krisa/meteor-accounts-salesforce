meteor-accounts-salesforce
============================

A meteor package for Salesforce's login service.

Package Dependencies
----------------------

* accounts-base
* accounts-oauth
* salesforce:salesforce

Install
-----------
```
meteor add salesforce:salesforce
```

Configuration
-----------

You can also add some configuration to the package:
```
Meteor.loginWithSalesforce({
	requestPermissions: ['full', 'id', 'chatter_api', 'api'],
	endPoint: 'test.salesforce.com'
}, function (err) {
	if (err) Session.set('errorMessage', err.reason || 'Unknown error');
});
```
By default, the scope is just 'api' and the endpoint is production ('login.salesforce.com')
