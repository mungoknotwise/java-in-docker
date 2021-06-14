## Lint
```
docker run --rm -i hadolint/hadolint < RuntimeDemo-Dockerfile.openjdk-11-jre-alpine
```

## Build
```
docker build -t runtime-demo:openjdk-11-jre-alpine-1 . -f RuntimeDemo-Dockerfile.openjdk-11-jre-alpine
```

## Examine (no UI)
```
CI=true docker run --rm -it -e CI=true -v /var/run/docker.sock:/var/run/docker.sock quay.io/wagoodman/dive:latest runtime-demo:openjdk-11-jre-alpine-1
```

## Examine (with UI)
```
docker run --rm -it -v /var/run/docker.sock:/var/run/docker.sock quay.io/wagoodman/dive:latest runtime-demo:openjdk-11-jre-alpine-1
```

## Vulnerability Scan
```
grype runtime-demo:openjdk-11-jre-alpine-1
```

## Run
```
docker run --rm -it runtime-demo:openjdk-11-jre-alpine-1
```
