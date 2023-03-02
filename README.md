Forked.

Not working on Mac M1/M2 ARM currently.

- `docker compose up`

Used `brew install chromium` on local mac (https://linguinecode.com/post/how-to-fix-m1-mac-puppeteer-chromium-arm64-bug)

See: https://github.com/pa11y/pa11y-dashboard/issues/253

```bash
pa11y-dashboard                              | [2023-03-02T09:50:17.029Z #59pdsY2FNr] Started GET / for ::ffff:172.23.0.1
pa11y-dashboard                              | 
pa11y-dashboard                              | Error: Could not connect to Pa11y Webservice
pa11y-dashboard                              |     at /dashboard/app.js:171:12
```


# pa11y-dashboard-docker-container
Docker Container with a auto updating pa11y-dashboard

## How to run

* docker compose up
* open your browser to localhost:4000

Container will everytime clone pa11y dashboard and install it. You should get a fresh and updated installation.

## How to edit

### about production.json

* mongo is the name of the container. it needs to match with the name of the service.

### about Dockerfile

* dependencies are required in order to permits puppeteer to work
* NODE ENV is required to handle what configuration file will be loaded from the service (in this case production.json)

### about updating

* sometime there are trouble that needs to make a docker rmi <image> and create again with docker compose up

