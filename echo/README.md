# Echo module

What does this ting do? It responds to http request on a given port at root (/) and sends back a JSON object in the body with some Radix information.

```Response object```

```
{
    "RADIX_APP": "",
    "RADIX_CLUSTERNAME": "",
    "RADIX_COMPONENT": "",
    "RADIX_ENVIRONMENT": "",
    "HOSTNAME": ""
}
```

## Local node development

Install dependencies (npm = node package manager)
```
npm install
```
Run the application
```
npm start
```
Run the application dev mode - automatic restart of server when changes in source code are detected.
```
npm run dev
```
Run a vulnerability check on dependencies
```
npm audit
```
Lint the Javascript code
```
npm run lint
```
Run the application in debug mode - extensive logging
```
npm run debug
```

### Environment variables

The echo application use the following environment variables:

* ```PORT``` to define which local port to listen to
* ```NODE_ENV``` with values ```development``` or ```production``` (used by the Express framework)

## Local docker development - build and run Echo

To build the image for the Echo app
```
docker build -t echo .
```

To run the Echo app in Docker
```
docker run -it --name=echo --rm -p 3000:3000 echo
```
(replace ```-it``` with ```-d``` to run in detached mode)