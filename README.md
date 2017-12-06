# dos-signpost-lambda

Presents signpost data over GA4GH compliant methods.

```                                                                                         
+------------------+      +--------------+        +----------------------------------------+
| ga4gh-dos-client |------|dos-gdc-lambda|--------|signpost.opensciencedatacloud.org/index |
+--------|---------+      +--------------+        +----------------------------------------+
         |                        |                                                         
         |                        |                                                         
         |------------------swagger.json                                                    
```

We have created a lambda that creates a lightweight layer that can be used to access data in signpost using GA4GH libraries.

The lambda accepts GA4GH requests and converts them into requests against requisite signpost endpoints. The results are then translated into GA4GH style messages before being returned to the client.

To make it easy for developers to create clients against this API, the Open API description is made available.

## Try it out!

Install chalice: `pip install chalice` and try it out yourself!

```
git clone https://github.com/david4096/dos-signpost-lambda.git
cd dos-signpost-lambda
chalice deploy
```


This will return you a URL you can make GA4GH DOS requests against!

For more please see the example notebook.

## TODO

* Validation
* Error handling
* Aliases
* Filter by URL
