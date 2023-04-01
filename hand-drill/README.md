# hand-drill
This is the docker image inherited from **Ubuntu 20.04** and built for the **debugging** purposes, especially the **web and network** related subjects. It includes mostly used tools and a **web server that listens the 8080** port.

Please visit the [`Dockerfile`](https://github.com/btungut/toolkit/blob/master/hand-drill/src/Dockerfile) for the details and included packages/applications.

## Run on docker
Execute the following snippet on your terminal to run hand-drill on your docker environment:

```bash
docker run -it -p 8080:80 btungut/hand-drill:0.3 bash
```

Or prefer the second option for not attaching the container:

```bash
docker run -d -p 8080:80 btungut/hand-drill:0.3
```

## Run on Kubernetes
To create **hand-drill** as a pod in your kubernetes cluster, please run the following command:

```
kubectl apply -f https://raw.githubusercontent.com/btungut/toolkit/master/hand-drill/deploy-kubernetes.yaml
```

> Before run the kubectl apply command, ensure the namespace you're working on!

## Source
Please visit the [github repository](https://github.com/btungut/toolkit/tree/master/hand-drill) for further details and source files.

## Tags (verisons)
Please visit the **tags** section of the [Docker Hub repository](https://hub.docker.com/r/btungut/hand-drill) to see available variations of the **hand-drill** docker image.

### Disclaimer
This application provided for the purpose of illustration and debugging only and is not intended to be used in a production environment.

THIS SAMPLE CODE AND ARTIFACTS AND ANY RELATED INFORMATION ARE PROVIDED "AS IS" WITHOUT 
WARRANTY OF ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED
TO THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A PARTICULAR 
PURPOSE.  