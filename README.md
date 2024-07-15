![logo](https://openelectricity.org.au/img/logo.svg)


# Capacity Parser

This is a jupyter notebook used for generating JSON representations of historical generation capacity.

It draws from the [au_facilities.json](https://data.dev.opennem.org.au/v3/geo/au_facilities.json) geoJSON file (from OpenNEM's dev environment) as well as historical solar PV data from [APVI](https://pv-map.apvi.org.au/data/postcode/monthly/capacity/).


## Output Files

* **Monthly and annual files by region**

  Monthly and annual JSON files are generated for each region, as well as for the NEM and for AU.

  Monthly values record the capacity in operation on the last day of the month, and are named `monthly.json`. Annual values record the capacity in operation on the first day of the financial year and are named `annual.json`.

  The files are stored in the `output` folder, under the `capacity` folder, in a heirarchy that mirrors the structure of the network and copies the structure of the energy/power files on OpenNEM.


* **Missing dates file**

  A CSV file `missing_dates.csv` is generated that contains the DUIDs for each facility for each region that has missing dates.


* **Unified annual file**

   A JSON file `unified_annual.json` is generated that contains the capacity in operation on the first day of the financial year for each facility for each region as well as a NEM and AU.


## Notes

* Currently the `network` attribute in the JSON files is capitalised, to mirror the (ad hoc?) convention of the current OpenNEM files.

## Contact

 File an issue or contact the author on Twitter at [@simonahac](https://twitter.com/simonahac)
