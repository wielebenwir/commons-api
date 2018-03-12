# commons-api
API for retrieving item information, availability and location of common goods item(s). 

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
