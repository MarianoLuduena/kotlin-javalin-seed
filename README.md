# kotlin-javalin-seed

## Requirements

- Java 11+

## Tracing instrumentation

```shell
java \
  -javaagent:{path-to-opentelemetry-agent.jar} \
  -Dotel.javaagent.configuration-file={path-to-opentelemetry-props-file} \
  ... some.jar
```

## Build

```shell
docker build -t kotlin-javalin-seed:latest --no-cache .
```

## Run

```shell
docker run --name javalin --rm -it -p 8080:8080 -m 256m --cpus="0.2" kotlin-javalin-seed:latest
```

## TODO

- [ ] Add tracing instrumentation to Docker image
- [ ] Coverage check with JaCoCo
- [ ] Upgrade to Javalin v5
- [ ] OAPI/Swagger generation
