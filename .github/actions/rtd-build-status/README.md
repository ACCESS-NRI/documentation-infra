# Get RTD build status

This action checks the latest `num-latest-builds` RTD builds for the project `rtd-project` and reports the status of the build triggered by commit `commit`. 

If the build succedes, it outputs the documentation and build URLs, if it fails it logs the failing error and URL build link.