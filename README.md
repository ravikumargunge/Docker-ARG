The `ARG` instruction alls you to define variables that can be passed at build time to customize the build process.

Syntax:

`ARG <name> [=<default value>]`

Example: `ARG VERSION=1` defines argument `VERSION` with a default value of `1.0`.

USAGE IN DOCKERFILE:
`ARG` is typically used to set up variables that can change between builds.

Example:

`FROM UBUNTU:20.041`
`ARG VERSION=1.0`
`RUN ECHO "Building version $VERSION"`

Passing Build Arguments:

`docker build --build-arg VERSION=2.0 -t myapp:2.0`


