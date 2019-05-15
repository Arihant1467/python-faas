# Python-FaaS(Function as a Service)
Using Open FaaS framework to build your own serverless functions using Docker and Kubernetes

# How to run
```
$ faas-cli build -f ./hello-python.yml
...

Successfully tagged hello-python:latest
Image: hello-python built.

$ docker images | grep hello-python
hello-python        latest       e0344b26305f     one minute ago

faas-cli push -f ./hello-python.yml

$ faas-cli deploy -f ./hello-python.yml
Deploying: hello-python.
No existing service to remove
Deployed.
200 OK
URL: http://127.0.0.1:8080/function/hello-python

$ curl 127.0.0.1:8080/function/hello-python -d "it's Alex here"
Hello! You said: its Alex here

```
# Reference
[Open FaaS](https://github.com/openfaas/faas)
