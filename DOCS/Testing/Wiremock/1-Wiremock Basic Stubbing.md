### Project Setup:

* Java 17
* Maven 3+
* Wiremock-standalone 3.9.2

### Basic Stubbing:

```json
{
  "request": {
    "method": "GET",
    "url": "/some/thing"
  },
  "response": {
    "status": 200,
    "statusMessage": "Everything was just fine!"
    "body": "Hello, world!",
    "headers": {
      "Content-Type": "text/plain"
    }
  }
}
```

### Stub priority: 

Note: When unspecified, stubs default to a priority of `5`  where `1` is the highest priority and Java `Integer.MAX_VALUE` (i.e., `2147483647`) is the minimum priority.

```json
{
    "priority": 1,
    "request": {
        "method": "GET",
        "url": "/api/specific-resource"
    },
    "response": {
        "status": 200
    }
}
```

### Sending response headers:

```json
{
    "request": {
        "method": "GET",
        "url": "/whatever"
    },
    "response": {
        "status": 200,
        "headers": {
            "Content-Type": "text/plain",
            "Set-Cookie": ["session_id=91837492837", "split_test_group=B"],
            "Cache-Control": "no-cache"
        }
    }
}
```

### Returning body using JSON file:

```json
{
    "request": {
        "method": "GET",
        "url": "/body-file"
    },
    "response": {
        "status": 200,
        "bodyFileName": "path/to/responseBody.json"
    }
}
```

Note: A response body in binary format can be specified as a `byte[]` via an overloaded `body()` in Java.

```json
{
    "request": {
        "method": "GET",
        "url": "/binary-body"
    },
    "response": {
        "status": 200,
        "base64Body": "WUVTIElOREVFRCE="
    }
}
```

### Default response for unmapped requests:

```json
{
    "priority": 10,
    "request": {
        "method": "ANY",
        "urlPattern": ".*"
    },
    "response": {
        "status": 404,
        "jsonBody": { "status": "Error", "message": "Endpoint not found" },
        "headers": {
            "Content-Type": "application/json"
        }
    }
}
```