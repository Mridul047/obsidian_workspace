### URL matching:

* Equality matching on path and query:

```json
{
  "request": {
    "method": "GET",
    "url": "/your/url?and=query"
  },
  "response": {
    "status": 200,
    "statusMessage": "Everything was just fine!",
    "body": "Hello, world!",
    "headers": {
      "Content-Type": "text/plain"
    }
  }
```

* Regex matching on path and query:

```json
{
  "request": {
    "method": "GET",
    "urlPattern": "/your/([a-z]*)\\?and=query"
  },
  "response": {
    "status": 200,
    "statusMessage": "Everything was just fine!",
    "body": "Hello, world!",
    "headers": {
      "Content-Type": "text/plain"
    }
  }
}```

* Equality matching on the path only:

```json
{
  "request": {
    "method": "GET",
    "urlPath": "/your/url"
  },
  "response": {
    "status": 200,
    "statusMessage": "Everything was just fine!",
    "body": "Hello, world!",
    "headers": {
      "Content-Type": "text/plain"
    }
  }
```

* Regex matching on the path only:

```json
{
  "request": {
    "method": "GET",
    "urlPathPattern": "/your/([a-z]*)"
  },
  "response": {
    "status": 200,
    "statusMessage": "Everything was just fine!",
    "body": "Hello, world!",
    "headers": {
      "Content-Type": "text/plain"
    }
  }
```


### Path templates:

* WireMock 3.0.0 onwards supports matching on URL path templates.
* When the path template URL match type is used this enables:
	* The ability to match path variables in the same way as query parameters, headers etc.
	* The ability to reference path variables by name in [response templates](https://wiremock.org/docs/response-templating/#the-request-model)

```json
{
  "request": {
    "method": "GET",
    "urlPathTemplate": "/customers/{customerId}/addresses/{addressId}"
  },
  "response": {
    "status": 200,
    "statusMessage": "Address matched!",
    "body": "Customer address 1",
    "headers": {
      "Content-Type": "text/plain"
    }
  }
```

* Path variable matching to specific value:

```json
{
  "request": {
    "method": "GET",
    "urlPathTemplate" : "/customers/{customerId}/addresses/{addressId}",
    "pathParameters" : {
      "customerId" : {
        "equalTo" : "504"
      },
      "addressId" : {
        "equalTo" : "01"
      }
    }
  },
  "response": {
    "status": 200,
    "statusMessage": "Address matched!",
    "body": "Customer address 1",
    "headers": {
      "Content-Type": "text/plain"
    }
  }
```

###  Matching other attributes:

* All request attributes other than the URL can be matched using the following set of operators.
* Equality:

```json
{
  "request": {
    "method": "GET",
    "url": "/ping",
    "headers": {
      "Content-Type": {
        "equalTo": "application/json"
      }
    } 
  },
  "response": {
    "status": 200,
    "statusMessage": "Everything was just fine!",
    "jsonBody": { "message": "System working fine@" },
    "headers": {
      "Content-Type": "application/json"
    }
  }
```

* Case-insensitive Equality:

```json
{
  "request": {
    "method": "GET",
    "url": "/ping",
    "headers": {
      "Content-Type": {
        "equalTo": "application/json",
        "caseInsensitive": true
      }
    } 
  },
  "response": {
    "status": 200,
    "statusMessage": "Everything was just fine!",
    "jsonBody": { "message": "System working fine@" },
    "headers": {
      "Content-Type": "application/json"
    }
  }
```

* Substring (contains) check:

```json
{
  "request": {
    "method": "GET",
    "url": "/ping",
    "cookies": {
      "my_profile": {
        "contains": "abc@gmail.com "
      }
    } 
  },
  "response": {
    "status": 200,
    "statusMessage": "Everything was just fine!",
    "jsonBody": { "message": "System working fine@" },
    "headers": {
      "Content-Type": "application/json"
    }
  }
```

* Negative substring (does not contain) check:

```json
{
  "request": {
    "method": "GET",
    "url": "/ping",
    "cookies": {
      "my_profile": {
        "doesNotContain": "abc@gmail.com "
      }
    } 
  },
  "response": {
    "status": 200,
    "statusMessage": "Everything was just fine!",
    "jsonBody": { "message": "System working fine@" },
    "headers": {
      "Content-Type": "application/json"
    }
  }
```

* Regex on query parameters:
```json
{
  "request": {
    "method": "GET",
    "url": "/ping",
    "queryParameters" : {
      "search_term" : {
        "matches" : "^[0-9]$"
      }
    }
  },
  "response": {
    "status": 200,
    "statusMessage": "Everything was just fine!",
    "jsonBody": { "message": "System working fine@" },
    "headers": {
      "Content-Type": "application/json"
    }
  }
```
