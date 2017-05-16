# mixed-content-scan

Just a simple docker wrapper for the awesome mixed content scanner by https://github.com/bramus/mixed-content-scan
I had trouble setting this up on OSX due to problems with curl, so installing it in a docker container is a pretty simple workaround.

## Usage

run this command to scan my website:

~~~bash
docker run -it --rm akiessling/mixed-content-scan https://powered-by-coffee.de
~~~

Or just save the warnings and errors to a log file on your computer with grep and tee
~~~bash
docker run -it --rm akiessling/mixed-content-scan https://powered-by-coffee.de |  tee >(grep -i -e "warn\|error" --line-buffered > ssl.log)
~~~
