## Docker Hub

The official pre-built image is available at https://hub.docker.com/r/jertel/elastalert-docker.

## Building Image Locally

To build, install Docker and then run the following command:
```
docker build . -t elastalert
```

## Running Elastalert container with docker hub repo

A properly configured elastalert_config.json file must be mounted into the container during startup of the container. Use the [example file](https://github.com/Yelp/elastalert/blob/master/config.yaml.example) provided by Elastalert as a template, and once saved locally to a file such as `/tmp/elastalert.yaml`, run the container as follows:

```bash
docker run --name {{name container}} -v {{absolute file path}}/config.yaml:/opt/config/elastalert_config.yaml -v {{Folder rules path}}/rules:/opt/elastalert/rules boyeuconnd/elast_alert
```