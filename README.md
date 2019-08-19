# testing-wiremock-docker
This is a simple POC for testing a wiremock-docker app.

## Testing
1. After cloning the repo, please run the following command to start the container:
`docker run -it --rm -p 8080:8080 -v $PWD:/home/wiremock rodolpheche/wiremock --verbose`

2. Testing by using the following curls:
- curl http://127.0.0.1:8080/hello |jq .
- curl -X POST http://127.0.0.1:8080/hello |jq .
- curl http://127.0.0.1:8080/hello?testing=WireMock |jq .
- curl --header "X-STUB: true" http://127.0.0.1:8080/hello |jq .
