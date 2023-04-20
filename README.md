# Log server #

This is the source for a log server image you can run on your platform of choice. It receives HTTP requests and logs them to STDOUT. Using e.g. `kubectl logs <podname> --follow` can follow the logs.

It's based on the standard NGINX image and uses the config to ensure all data is logged to the stdout

## Steps ##

1. Build the image from the image folder using: `docker build -t janjaapz/log-server:latest .` or any tag you like. Alternatively you can pull the image from docker hub
2. When your build is complete use the attached deployment and service to rollout the server to your container platform, `kubectl apply -f log-server-deployment.yaml` and `kubectl apply -f log-server-service.yaml` you might want to change the namespace and servicetype first.
3. Finally when the resources are applied, check the name of the pod using `kubectl get pods` and `kubectl logs <podname> --follow` to follow any requests sent to this pod.