# Commons API

API for retrieving item information, availability and location of common good item(s).

![](img/portal.png)

This project aims to create a standard format for exchanging information between  software used by grassroots organisations to lend common goods. Based on this API, an open source "Commons Hub" software package is in development. The "Commons Hub" allows users to browse the items that all participating initiatives are offering.  

By design, the API will not be collecting/sharing any user data, individual projects will remain in total control. 

## Contributing

We are looking for contributers, both developers and sharing initiatives. 


## Implementation

As a first step, we are working to implement the API into 2 projects that are already widely used to share cargo bikes:

* Booking software: [Commons Booking](https://github.com/wielebenwir/commons-booking-2) (Wordpress Plugin, used by over 60 sharing initiatives) 
* Hub: [velogistics.net](http://velogistics.net) (Cargobike-sharing portal with more than 250 available bikes)

Commons Booking provides initiatives with a tool to manage and lend common goods, the successor of velogistics will serve as the hub connecting the individual installations.



## Draft

Example of a json return for a bike from the commons cargobike project http://kasimir-lastenrad.de.


```

"project" {
	"name" : "Kasimir Project",
	"url" : "https://kasimir-lastenrad.de",
	"description" : "The first!",
	"image" : "https://kasimir-lastenrad.de/logo.png",
	"id": 1,
	"publish_on_velo" : true/false,
	"site_language" : "DE",
	"meta_schema" : "https://github.com/wielelbenwir/commons-api.js"
}

"location" {
	"latitude" : 32.888,
	"longitude" : 57.987,
	"name" : "Nice Cafe",
	"id" : 34
}

"item" {
	"name" : "Kasimir",
	"availability" [
		{
			"slot_start": "09:00", // full date and time timestamp
			"slot_end" : "13:00",
			"standort_id" : 27,
			"available": true/false
		} ...

	],
	"description" : "This is a great bike",
	"meta" {
		"gears" : 3, // optional
		"max_loading_weight_kg" : 100,
		"type_of_bike" : "three_wheels", // send a slug, localise at either end, we select the slugs
		"size_of_box" : "big", 
		"ebike" : true / false,
		"children" : true / false,
		"tags" : [
			"fun in the sun", "birthdays" // user generated content
		]
		...
	},
	"owner_id" : 1,
	"item_url" : "https://fun.com/kasimir",
	"item_image" : "https://fun.com/wp-content/uploads/2018/02/kasimir.jpg",

}
```
