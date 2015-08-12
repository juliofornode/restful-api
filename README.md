
Basic MEAN Stack Project: RESTful API
===

[Link to live project](https://warm-brushlands-1881.herokuapp.com/)

0. Goals
---
* Single-page CRUD app to manage a contact list
* Basic usage of the four components of the MEAN stack
* Usage of mongojs to integrate Mongo and Node


1. Start With an Html & Bootstrap Mock Up
---
* HTML skeleton
* Bootstrap CSS from CDN


2. Add Angular to Prototype the App
---
* Add Angular script from CDN
* Declare ng app in /controllers/controller.js
* Set ng controller and scope
* Add ng directives

* To clear the input field and refresh the data list as soon as a new item is entered

```
var refresh = function () {

	$http.get('/contactlist')
	.success(function(response) {
		$scope.contactlist = response
	})
	
	$scope.contact = ""
}

refresh()

$scope.addContact = function() {
			$http.post('/contactlist', $scope.contact)
			.success(function(response) {
				console.log(response)
				refresh()
			})

}
```


3. Set the Server With Node and Express
---
* Install express and body-parser
* Create basic server
* Create basic get/post api


4. Run Mongo Deamon, Create db, use mongojs to Connect
---
* mongod
* install mongojs
* update api with mongojs


5. Use $http to Connect ng to Node
---
* Update Angular: add $http as dependency of the controller
















