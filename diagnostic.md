# Ember Routing Diagnostic

Record your responses inside the fenced code blocks below each question.

1.  What are the main task(s) you perform inside the Ember Application Router,
    and what are the main task(s) you perform inside an Ember Route?

    ```md
    <!-- your response here -->
    router is for the different url paths. Route is for the  data within a
    url path and putting it into an object.
    ```

1.  What is the command to generate a route named `boston` nested under
    `campus`?

    ```md
    <!-- your response here -->
    ember generate route /campus/boston
    ```

1.  Suppose you have a nested route at the URL `/campus/boston`. How would you
    use the `link-to` helper to generate an appropriate link?

    ```md
    <!-- your response here -->
    {{#link-to 'boston' boston}}
    {{boston}}{{/link-to}}
    ```

1.  Explain **at least** two differences between the following two route
    definitions.

    ```js
    this.route('products', function () {
      this.route('product', { path: '/:product_id' }); // <= 👀here
    });

    this.route('product', { path: '/products/:product_id' }); // <= 👀 here
    ```

    ```md
    <!-- your response here -->
    one is nested within products, one is not nested. One is a route path of
    products, one is of product.
    ```

1.  Suppose we have the following route definition:

    ```js
    this.route('movie', { path: '/movies/:movie_id' }); // <= 👀 here
    ```

    If we navigate in the browser to `/movies/123`, how can we reference the
    value `'123'` inside a Route?

    ```md
    <!-- your response here -->
    I am not entirely sure what you mean by 'value'.
    here is how you would get to that route in the router

    this.route('movie', { path: '/movies/:movie_id'});

    and in the template you could reference the value 123 like this.
    {{#link-to 'movie' movie}}{{movie._id.123}}{{/link-to}}</li>


    ```

1.  Inside a template, how do we reference data provided by a Route?

    ```md
    <!-- your response here -->
    you reference sort of like how in mongo. like object.attribute. So say you have
    a house route that has attribute diningRoom it'd be referenced like
    {{house.diningRoom}} in handlebars moustaches.
    ```
