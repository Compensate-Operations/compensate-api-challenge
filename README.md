# compensate-api-challenge

## Background

At Compensate we are on our way building a fleet of services to make the one-stop-shop for carbon compensation a reality.

Most of those services will be interfacing with each other using [RESTful](https://en.wikipedia.org/wiki/Representational_state_transfer) APIs, 
this is something surely you have heard about before.

Building a carbon calculation algorithm or a machine-learning solution would surely proof your technical skills to help us building Compensate's
ambitious architectural vision, however, we think that would be an overshoot so we would like to see something more self-contained where you can 
potentially show us how you reason and build solutions.

For this challenge, we would like you to build a very small service exposing an API to manage Compensate's products.

A product for Compensate is an item tied to a tangible product that models the [carbon footprint](https://en.wikipedia.org/wiki/Carbon_footprint) that
the said tangible product costs to the environment. Thus, for Compensate it is very important to have a service to manage such.

A product for Compensate looks roughly like below

```
    {
      "id": "8381a025-61fc-4479-b335-cc60b0b87b60",
      "name": "Generic cotton t-shirt",
      "properties": {
        "label": "textile, cotton",
        "value": 2.01,
        "unit": "Kg",
        "context": {
          "origin": "India",
        }
      },
      "parent_id": "",
      "created_at": "2020-04-29T12:57:08+00:00"
      "modified_at": "2020-04-29T12:57:08+00:00"
    }

```

Note that it is possible to create hierarchies of products making use of the `parent_id` to reference another product. For more, see [sample data](./data.json) attached.

The small service must manage products, that is, via its interface a user should be able to create a product, list all products and retrieve a product.

## Task

We would like you to build a very minimal service to manage a product listing with the following characteristics:

- A RESTful interface to create, update and list products as well the information for a single product.
- A specific endpoint to lookup a specific product.
- A description of the API following [OpenAPI specification](https://github.com/OAI/OpenAPI-Specification).

Some things to keep in mind:

- The main goal of the challenge is for you to demonstrate your thinking when designing and writing an API.
- The solution should aim to be maintainable and scalable.
- Choose your own tools (i.e.: use the language you feel most comfortable with as long as it can fulfill the requirements above).
- For simplicity, authentication and authorization are out of the scope of this challenge.
- Data persistency layer is out of the scope

## Bonus

- Given the above described API, enhance it making use of HTTP's [HEAD](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods/HEAD) verb.
- How would you implement the feature of adding a new product as a child of an already existing product? (i.e. which method to use, how to link it, etc)

## Things we will be looking at

- The attention to detail when designing and implementing the API.
- The maintainability of the code.

## Things we will NOT be paying attention to

- A given framework or language choice.
- A solution going over the mark (i.e. implement authentication or data persistency).

## Submitting a solution

You may fork this repository freely and hack on. In order to submit your solution, you may:

a) Send a link to your private Github repo hosting a solution for this challenge to `engineering@compensate.com`. We will contact you soon after.

b) Send us a zipped folder containing a solution for this challenge. Contact details below.

## Contact

If you have questions regarding the challenge (and you are too shy to open an Issue) please don't hesitate to contact `engineering@compensate.com`. We will get back to you as soon 
as possible.
