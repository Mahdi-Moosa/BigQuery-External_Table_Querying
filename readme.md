# Objective

EL pipeline to compare different approaches to querying external data in BigQuery.

# Codes

The repo provides extraction load pipeline to read NY Taxi CSV data (source: https://github.com/DataTalksClub/nyc-tlc-data/releases/tag/fhv) and load to GCS bucket. Two python scripts are:

* from_web_to_gcs_parquet.py : Reads csv.gz file(s) and writes parquet file(s) to gcs.
* from_web_to_gcs_orc.py : Reads csv.gz file(s) and writes ORC file(s) to gcs.