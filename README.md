# nspy_wrapper
A Python wrapper for the NationStates API.

## Overview
nspy_wrapper (pronounced "*n-spy wrapper*", installed as ``nspywrapper``) is an open source library allowing Python applications to access the NationStates API with minimal effort.
nspy_wrapper has the following features:
* a fully functional interface for the NationStates API v11 including the Nation, Region, World, World Assembly, Telegrams, Trading Cards and Verification APIs
* automatic rate-limiting to avoid losing access, including longer ratelimits for the Telegrams API
* XML decoding and reading - all data is converted to python structures in dict and list format

## Usage
nspy_wrapper is installable via pip, using the following command:
``pip install nspywrapper``

Once it's installed, it can then be included in any program like any other library. (``import nspywrapper``; ``from nspywrapper import *``) 

### Components
nspy_wrapper includes the following component classes:
#### nsRequests
nsRequests is the main component, handling all ratelimiting, requesting and interfacing. It will import nsParser, nsResponse and all necessary exceptions.
#### nsParser
nsParser is a fully functional XML parsing system designed to work with data returned from the NS API. While nsParser does not require an API version to be provided, it may encounter errors in parsing data from an unsupported API version.
#### nsResponse
nsResponse is a formatting object that defines the response from the Nationstates API. It is similar in format to a requests.Response object.

### Examples
For example usage, look at my other NS repositories and projects, all of which are written using nspy_wrapper.

## License
nspy_wrapper is licenced under the Apache License 2.0.
