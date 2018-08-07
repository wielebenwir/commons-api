# Commons API

API for retrieving item information, availability and location of common good item(s), defined as a [JSON schema](http://json-schema.org/).

![](img/portal.png)

This project aims to create a standard format for exchanging information between software used by grassroots organisations to lend common goods. Based on this API, an open source "Commons Hub" software package is in development. The "Commons Hub" allows users to browse the items that all participating initiatives are offering.

By design, the API will not be collecting/sharing any user data, individual projects will remain in total control.

## Contributing

We are looking for contributers, both developers and sharing initiatives.

* [Join our mailing list](https://ml06.ispgateway.de/mailman/listinfo/commons-api_wielebenwir.de)

## Implementation

As a first step, we are working to implement the API into 2 projects that are already widely used to share cargo bikes:

*   Booking software: [Commons Booking](https://github.com/wielebenwir/commons-booking-2) (Wordpress Plugin, used by over 60 sharing initiatives)
*   Hub: [velogistics.net](http://velogistics.net) (Cargobike-sharing portal with more than 250 available bikes)

Commons Booking provides initiatives with a tool to manage and lend common goods, the successor of velogistics will serve as the hub connecting the individual installations.

## Draft

The API is defined in a [JSON schema](https://github.com/wielebenwir/commons-api/blob/master/commons-api.schema.json) in this repository. We have used schema descriptions to self-document the format. You can use the [JSON schema validator](https://www.jsonschemavalidator.net/) to try out the schema. Just paste the file content into the left field and start to compose your first Commons API data.

[TODO]: Add Example of a json return for a bike from the commons cargobike project http://kasimir-lastenrad.de.
