SonarQube docker build. (See docker-compose.yml)

## Instructions

run `docker-compose -up -d`

```
    In your browser, connect to localhost:9000
    Default
        Username = admin
        Password = admin
```

To install sonar scanner on linux, you can use the provided script `./scripts/install-sonar-scanner`.

### To run the scanner, you can use this sample code

```
sonar-scanner \
  -Dsonar.projectKey={PROJECT_KEY} \
  -Dsonar.sources=. \
  -Dsonar.host.url=http://localhost:9000 \
  -Dsonar.token={PROJECT_TOKEN_ID}
```

Make sure you change the PROJECT_KEY and the PROJECT_TOKEN_ID above to match the provided values inside the SonarQube UI (per your project configuration).
