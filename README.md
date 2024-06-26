# FRDR Registry Data
Static data used in FRDR taken from authority registries

Data files must be JSON format. At present only [ROR version 2 schema](https://ror.readme.io/v2/docs/data-structure) is supported.

Data files cannot be renamed as there are automated processes that expect them to have a certain name in this repo.

## Updating ROR Data in this repo

1. Locate the latest [ROR data dump](https://ror.readme.io/docs/data-dump) it will be on Zenodo
2. Download the Zip file of this dataset, it will be named something like `v1.45.1-2024-04-18-ror-data.zip`
3. Unzip the downloaded file
4. Rename the file from `v1.45.1-2024-04-18-ror-data_schema_v2.json` to `ror_v2.json` (<b>important to choose schema_v2 file here!</b>)
5. Zip `ror_v2.json` into `ror_v2.zip` (if on a Mac, use the -X flag like this: `zip -X ror_v2.zip ror_v2.json`)
6. Move `ror_v2.zip` into your local copy of this repo
7. Commit and push

## Updating ROR Data in a Globus Publish environment

1. Deploy the site.yml playbook using keyword `orgregistry`
2. Log into the web VM, become user dspace, and run:

* `/dspace/bin/dspace org-registry delete`
* `/dspace/bin/dspace org-registry load`
