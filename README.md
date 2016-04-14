Docker-Hyperledger
===
Base Docker images for [Hyperledger](https://www.hyperledger.org).

# Supported tags and respective Dockerfile links

* [`0.1, latest` (latest/Dockerfile)](https://github.com/yeasy/docker-hyperledger/blob/master/Dockerfile)

For more information about this image and its history, please see the relevant manifest file in the [`yeasy/docker-hyperledger` GitHub repo](https://github.com/yeasy/docker-hyperledger).

# What is docker-hyperledger?
Base Docker image with hyperledger deployed. Your can see [hyperledger-peer](https://hub.docker.com/r/yeasy/hyperledger-peer/) if you want to deploy a hyperledger cluster.

# How to use this image?
The docker image is auto built at [https://registry.hub.docker.com/u/yeasy/hyperledger/](https://registry.hub.docker.com/u/yeasy/hyperledger/).

## In Dockerfile
```sh
FROM yeasy/hyperledger:latest
```

## Local Run
The image will automatically run the peer, add your sub command and flags at the end.

E.g., see the supported sub commands with the `help` command.
```sh
$ docker run --rm -it yeasy/hyperledger fabric help
06:08:01.446 [crypto] main -> INFO 001 Log level recognized 'info', set to INFO


Usage:
  peer [command]

Available Commands:
  peer        Runs the peer.
  status      Returns status of the peer.
  stop        Stops the running peer.
  login       Logs in a user on CLI.
  network     Lists all network peers.
  chaincode   chaincode specific commands.
  help        Help about any command

Flags:
      --logging-level="": Default logging level and overrides, see core.yaml for full syntax


Use "peer [command] --help" for more information about a command.
```

# Which image is based on?
The image is built based on [golang:1.6](https://hub.docker.com/_/golang) image.

# What has been changed?
## install dependencies
Install required  libsnappy-dev, zlib1g-dev, libbz2-dev.

## install rocksdb
Install required  rocksdb 4.1.

## install hyperledger
Install hyperledger and build the fabric as peer 

# Supported Docker versions

This image is officially supported on Docker version 1.7.0.

Support for older versions (down to 1.0) is provided on a best-effort basis.

# Known Issues
* N/A.

# User Feedback
## Documentation
Be sure to familiarize yourself with the [repository's `README.md`](https://github.com/yeasy/docker-hyperledger/blob/master/README.md) file before attempting a pull request.

## Issues
If you have any problems with or questions about this image, please contact us through a [GitHub issue](https://github.com/yeasy/docker-hyperledger/issues).

You can also reach many of the official image maintainers via the email.

## Contributing

You are invited to contribute new features, fixes, or updates, large or small; we are always thrilled to receive pull requests, and do our best to process them as fast as we can.

Before you start to code, we recommend discussing your plans through a [GitHub issue](https://github.com/yeasy/docker-hyperledger/issues), especially for more ambitious contributions. This gives other contributors a chance to point you in the right direction, give you feedback on your design, and help you find out if someone else is working on the same thing.
