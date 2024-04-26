### Version 
If you wanna to use `docker init`, the docker's version need 20.10.0+.

### Generative Dockerfile by docker init
`docker init`

### Choice one of the application platform for your project use, 

we are using `python`, you will get those file:

```
total 40
-rw-r--r--  1 kennywarwick  staff   1.0K Apr 25 23:39 README.Docker.md
-rw-r--r--  1 kennywarwick  staff    15B Apr 25 23:11 requirements.txt
-rw-r--r--  1 kennywarwick  staff   1.6K Apr 25 22:24 compose.yaml
-rw-r--r--  1 kennywarwick  staff   1.6K Apr 25 22:24 Dockerfile
-rw-r--r--  1 kennywarwick  staff   187B Apr 25 22:24 app.py
```

### Building and running your application

When you're ready, start your application by running:
`docker compose up --build`.

> Remember to add `gunicorn` on requirements.txt

Your application will be available at http://localhost:5000.

### Deploying your application to the cloud

First, build your image, e.g.: `docker build -t myapp .`.
If your cloud uses a different CPU architecture than your development
machine (e.g., you are on a Mac M1 and your cloud provider is amd64),
you'll want to build the image for that platform, e.g.:
`docker build --platform=linux/amd64 -t myapp .`.

Then, push it to your registry, e.g. `docker push myregistry.com/myapp`.

Consult Docker's [getting started](https://docs.docker.com/go/get-started-sharing/)
docs for more detail on building and pushing.

### References
* [Docker's Python guide](https://docs.docker.com/language/python/)
* [Docker init blog](https://medium.com/kpmg-uk-engineering/you-should-stop-writing-dockerfiles-today-do-this-instead-3cd8a44cb8b0)
* [Docker init sample](https://docs.docker.com/reference/cli/docker/init/)
