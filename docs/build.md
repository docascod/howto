# Build your document

?> Build process transforms source document (md,rst, ...) into definitive document (pdf, epub) applying configuration and selected theme.



DAC docker image embed all commands (build, assemble). You must choose one on first parameter.

````docker
docker run docascod/docsascode:latest build
````

You must indicated files to build. To do that, you must set a volume and add filename in parameters :

````docker
docker run -v $PWD/:/documents/ docascod/docsascode:latest build mydocument.md
````

 You can build several documents in several format within a single command :

````docker
docker run -v $PWD/:/documents/ docascod/docsascode:latest build mydocument.md seconddocument.rst
````

````docker
docker run -v $PWD/:/documents/ docascod/docsascode:latest build *.md *.rst
````

## Environment variables

`DEFAULT_DESTINATION`  : Path to output definitive document. Default value : source file folder. 

!> This path must be visible from the volume set in docker command.

`DEFAULT_OUTPUT` : Document output format if not set in metadata ([See output description](output.md))

````docker
docker run -e DEFAULT_OUTPUT=output.slides -e DEFAULT_LOCATION=/documents/build/ -v $PWD/:/documents/ docascod/docsascode:latest build mydocument.md
````



## Build with github actions

coming soon ...

## Build in Gitlab CI

coming soon ... 