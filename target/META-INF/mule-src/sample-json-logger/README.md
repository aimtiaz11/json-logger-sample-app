# json-logger-sample-app


API call:

```
curl --location --request POST 'localhost:8081/api/v1/log' \
--header 'Content-Type: application/json' \
--data-raw '{
	"test": "value"

}'
```

Log output:

```
DEBUG 2020-02-03 18:21:51,392 [[MuleRuntime].io.07: [sample-json-logger].sample-json-loggerFlow.BLOCKING @61ebf6ac] [event: d5c3b9c0-4655-11ea-ad05-8c04ba7dd095] org.mule.extension.jsonlogger.JsonLogger: {
  "applicationName" : "sample-json-logger",
  "applicationVersion" : "1.0",
  "environment" : "dev",
  "tracePoint" : "START",
  "timestamp" : "2020-02-03T07:21:50.760Z",
  "elapsed" : "3",
  "locationInfo" : {
    "lineInFile" : "20",
    "component" : "json-logger:logger",
    "fileName" : "sample-json-logger.xml",
    "location" : "sample-json-loggerSub_Flow/processors/0",
    "rootContainer" : "sample-json-loggerSub_Flow"
  },
  "threadName" : "[MuleRuntime].io.07: [sample-json-logger].sample-json-loggerFlow.BLOCKING @61ebf6ac",
  "content" : {
    "payload" : {
      "test" : "value"
    },
    "attributes" : {
      "headers" : {
        "content-type" : "application/json",
        "user-agent" : "PostmanRuntime/7.22.0",
        "accept" : "*/*",
        "cache-control" : "no-cache",
        "postman-token" : "707a35ad-8930-4d05-bdd2-a6a209b9bd6c",
        "host" : "localhost:8081",
        "accept-encoding" : "gzip, deflate, br",
        "content-length" : "21",
        "connection" : "keep-alive"
      },
      "method" : "POST",
      "scheme" : "http",
      "queryParams" : { },
      "requestUri" : "/api/v1/log",
      "queryString" : "",
      "version" : "HTTP/1.1",
      "maskedRequestPath" : "/",
      "listenerPath" : "/api/v1/log/*",
      "relativePath" : "",
      "localAddress" : "/127.0.0.1:8081",
      "uriParams" : { },
      "rawRequestUri" : "/api/v1/log",
      "rawRequestPath" : "/api/v1/log",
      "remoteAddress" : "/127.0.0.1:62458",
      "requestPath" : "/api/v1/log"
    }
  }
}
```