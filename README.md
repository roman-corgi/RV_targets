# nearby_rv_exoplanets

	
For ease of viewing on github the ecsv header and the raw table are
stored as seperate files.

Use this snippet to load as a astropy table with units:

	from astropy.table import Table
	latest_params_fname = "RV_targets/LatestRVmeasurements.csv"
	ecsv=open(latest_params_fname+".header").readlines()+open(latest_params_fname).readlines()
	Table.read(ecsv,format="ascii.ecsv")
