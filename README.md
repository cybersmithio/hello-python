# hello-python
This project serves as an example of how to integrate Travis CI with Tenable.io Container Security.  A very simple Docker image
using Python 2.7.16, which should have at least one vulnerability so you'll have something to see in the results.  The YAML file
instructs Travis CI to build the image, download the Tenable.io on-premise container inspector, run the image through the inpsector, 
and then wait for the results using the tiocs-check.sh

