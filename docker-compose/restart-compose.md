## Restarting app with newer images

If you have released a new version of Docker image or just need to update the current running image of a docker-compose, use this guide.

1. Stop the running docker-compose:

```bash
docker-compose down
```

This will stop all the running containers. Make sure that you are stopping the correct app, as this one will stop the app generated
from the default `docker-compose.yml` file. In other words, if you run your app from, let's say, `production.yml`, don't forget to add 
`-f production.yml` flag.

2. Pull/build new images

```bash
docker-compose pull
```
This will pull the newer versions of all images that your app uses from the Docker Hub. It is possible to pull specific images by providing
the name of the service as the argument:
```bash
docker-compose pull backend nginx
```

3. Restart/start
```bash
docker-compose up -d
```
This will start your app in the background. If you need to debug your app and want to see the logs, omit the `-d` flag.
