This repo is a fork of https://github.com/iannuttall/binlist-data

The BIN data in the repo is exposed as a RESTful API using a simple Flask frontend. 

A docker image can be created by running the command

docker build --tag binlookup . 

To run the docker image, you can run the command below (to expose the lookup service on a port different from 5000, (say 8000), change the -p option to 8000:5000

docker run --name binlookup -d -p 5000:5000 binlookup


The service can be used to do BIN lookups by sending a GET request to /lookup/&lt;credit-card-number&gt; (its enough to send just the first 6 digits)

ex: http://localhost:5000/lookup/377420

You are free to use this list for any purpose, including private or commercial use. This is just a test project, so use at your own risk. 
