# Log server #

This is the source for a log server image you can run on your platform of choice. It receives HTTP requests and logs them to STDOUT. Using e.g. kubectl you can follow the logs.

It's based on the standard NGINX image and uses the config to ensure all data is logged to the stdout

## Steps ##

1. Build the image from the image folder using: `**docker build -t janjaapz/log-server:latest .**` or any tag you like. Alternatively you can pull the image from docker hub
2. 