# hello-python
This project serves as an example of how to integrate Travis CI with Tenable.io Container Security.  A very simple Docker image
using Python 2.7.16, which should have at least one vulnerability so you'll have something to see in the results.  The YAML file
instructs Travis CI to build the image, download the Tenable.io on-premise container inspector, run the image through the inpsector, 
and then wait for the results using the tiocs-check.sh

# Usage
If you try using the project as-is, you will need to replace the three "secure" lines in the .travis.yml file with your own variables:
   TENABLE_IO_ACCESS_KEY
   TENABLE_IO_SECRET_KEY
   TENABLE_JFROG_PASSWORD 


A simple way to do this is just delete the secure lines and then run the travis encrypt commands like this:
'''
travis encrypt TENABLE_IO_ACCESS_KEY=_________________ --add
travis encrypt TENABLE_IO_SECRET_KEY=_________________ --add
travis encrypt TENABLE_JFROG_PASSWORD=_________________ --add
'''
This will automatically update the .travis.yml file using your encryption keys.