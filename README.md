# FRDR Registry Data
Static data used in FRDR taken from authority registries

Data files must be CSV format.  Column order:
id,country_code,name_en,name_fr,altnames

* **id**: the item unique ID from the registry; usually starts with "http" or "https"
* **country_code**: 2 letter ISO 3166 code, upper case. See https://www.iso.org/iso-3166-country-codes.html
* **name_en**: The English display name for the item. If the name contains a comma it must quoted.
* **name_fr**: The French display name for the item. If the name contains a comma it must quoted.
* **altnames**: A delimited list of all alternatives names for the item. The delimiter pattern is set in the configuration table org_registries, so it may vary by registry. Any names that contain the delimiter pattern or a comma must be quoted.

Data files cannot be renamed as there are automated processes that expect them to have a certain name in this repo.
