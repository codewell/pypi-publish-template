# pypi publish template

A simple template for a cli to publish python libraries in a safe and consitent way to pypi.

It runs tests and ensure a clean repo before publish and handles the git tagging of the release in a sane way.


## Requirements

* git
* python
* twine
* pytest

## How to setup

* Copy `publish.sh` to the project root
* Replace `<package-name>` with the name of the library.

## How to use

To publish version `0.13.37`

* Run `./publish.sh 0.13.37`
* Follow instructions
* The script will only push the git tags if the tests pass
* The script will try its best to clean up the git state after itselves when it fails, but this is not a guarantee, double check with `git status` when recovering after a failure.
