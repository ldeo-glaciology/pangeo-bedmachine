load_plot_bedmachine is a simple notebook for lazily loading an analyzing bedmachine data.
It includes code for starting a cluster in ooi.pangeo.io, but it works without this too, its just slow.

nc_to_zarr is an attempt to save both the bedmachine data and a pism output netcdf into zarr

intake_catalog_setup creates an intake catalog for the data. Now anyone can load these data using 

cat = intake.open_catalog('https://raw.githubusercontent.com/ldeo-glaciology/pangeo-bedmachine/master/bedmachine.yaml')
bm_from_intake  = cat["bedmachine"].to_dask()
