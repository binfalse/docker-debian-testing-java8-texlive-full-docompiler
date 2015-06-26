# docker: DOCOMPILER
An image based on [binfalse/d-java8-texlive-full:1.0](https://registry.hub.docker.com/u/binfalse/d-java8-texlive-full/). This image has a [Java 8 runtime environment](http://openjdk.java.net/projects/jdk8/) (Debian's `openjdk-8-jre`) and the [full texlive distribution](http://www.tug.org/texlive/) (Debian's `texlive-full`) installed.

In addition, the [DOCOMPILER](https://github.com/binfalse/DocumentObjectCompiler) tool is deployed. The image defines an entry point to immediately run the Document Object compiler. Given a Document Object in `/tmp/myproject/do.zip` you can obtain the PDF by calling:

    docker run --rm -v /tmp/myproject:/job binfalse/docompiler:1.0 /job/do.zip

You'll find the resulting PDF and the pdflatex output in `/tmp/myproject/`.

Read more about the [docompiler tool](https://github.com/binfalse/DocumentObjectCompiler).

