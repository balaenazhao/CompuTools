# Descriptions of data normalization for cranes.csv
## Original data sheet contains 151 specimen records and 24 fields.

This large table can be divided into 4 tables (museum, taxonomy, specimen and country), to reduce redundancy and increase readability.
Multiple specimens can be stored in the same museum, which has the same contact person and email.
One species can have multiple specimens, therefore taxonomic info would be redundant across the specimens from the same species.
Multiple specimens from the same or different species can come from the same country and continent, so a country table can reduce a lot of repetitive info.

Table **museum** 

Column header | Data type
--------------|----------
name | string
code | string
contact | string
email | string


Table **taxonomy**

Column header | Data type
--------------|----------
name | string
kingdom | string
phylum  | string
class | string
order | string
family | string
genus | string
specific_epithet | string


Table **specimen**

Column header | Data type
--------------|----------
ID | int
scientific_name | string
museum_code | string
sex | string
lifestage | string
mass | float
country_code | string
state | string
county | string
locality | string
elevation | float
date | string


Table **country**

Column header | Data type
--------------|----------
code | string
name | string
continent | string
