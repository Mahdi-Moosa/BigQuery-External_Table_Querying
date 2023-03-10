# Objective

EL pipeline to compare different approaches to querying external data in BigQuery. Compares between:
* Importing data as non-partitioned BigQuery table
* Importing data as partitioned BigQuery table
* Query data as external table (csv.gz file)
* Query data as external parquet file. Here, three different parquet compression formats were compared.
    * snappy compression
    * gzip comporession
    * brotli compression
* Query data as external ORC file. 

Results of the comparson is discussed here: [link](https://mahdimoosa.substack.com/p/comparing-different-approaches-to).

# Codes

The repo provides extraction load pipeline to read NY Taxi CSV data (source: https://github.com/DataTalksClub/nyc-tlc-data/releases/tag/fhv) and load to GCS bucket. Two python scripts are:

* *from_web_to_gcs_parquet.py* : Reads csv.gz file(s) and writes parquet file(s) to gcs.
* *from_web_to_gcs_orc.py* : Reads csv.gz file(s) and writes ORC file(s) to gcs.

# Link to relevant blog:
* Comparing Different Approaches to Querying External Data in BigQuery: [link](https://mahdimoosa.substack.com/p/comparing-different-approaches-to)

## Schematic outline:

![My Image](images/BigQuery_External_Table.jpg)
