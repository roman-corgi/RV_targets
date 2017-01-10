# nearby_rv_exoplanets


[LatestRVmeasurements.csv](LatestRVmeasurements.csv)  defines astrophysically measured
quantities of nearby RV exoplanets of interest to WFIRST.

[LatestRVmeasurements.csv.header](LatestRVmeasurements.csv.header) defines the units of each column in [ecsv](https://github.com/astropy/astropy-APEs/blob/master/APE6.rst) format. 

This list was originally compiled by Nikole Lewis (STScI) for the
 WFIRST CGI SITs.
	
For ease of viewing on github the [ecsv](https://github.com/astropy/astropy-APEs/blob/master/APE6.rst) header and the raw table are
stored as seperate files.

Use this snippet to load as an [astropy](http://www.astropy.org) table with units:

	from astropy.table import Table
	latest_params_fname = "RV_targets/LatestRVmeasurements.csv"
	ecsv=open(latest_params_fname+".header").readlines()+open(latest_params_fname).readlines()
	Table.read(ecsv,format="ascii.ecsv")

