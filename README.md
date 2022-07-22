# Nodejs Hello World

This is a very basic Node Hello World application that serves the value of the application property `message` via the web. While simple it's designed to show off some of the kubernetes functionality.

## Quick Start

Clone the repo down locally:

```console
git clone 
cd nodejs-app
```

Assuming you have Nodejs installed you can run it with:

```console
$ npm install 
```

Point your web browser or use wget/curl/httpy at `localhost:8080`:

```console
$ http localhost:8080
HTTP/1.1 200
Content-Length: 17
Content-Type: text/plain;charset=UTF-8
Date: Wed, 27 Feb 2019 21:13:35 GMT

hello development
```

## Build and Run

### With Docker

If you have Docker you can skip using Maven and Java and Build a docker image:

```console
$ docker build -t nodejs-hello .
...
...
Successfully built 5405805d6f47
Successfully tagged nodejs-hello:latest
```

Run it:

```console
$ docker run --name nodejs-hello -d --rm -p 8080:8080 nodejs-hello
6d47dc1ea4833f1a68c6969d4969a74a4d656b9a85600fd089b3cf0ca9716b9d

$ curl localhost:8080
hello world

$ docker rm -f spring-hello
```
