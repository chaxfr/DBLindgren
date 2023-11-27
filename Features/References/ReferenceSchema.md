# Reference Schema
* This document shall contain a definition for the schema used for references.
* It shall contain a specification of the algorithm used to export references from the database.  
* It shall also be able to export all incidents tied to a research project into a table format.
* This table format shall contain text snippets useable for footnotes in an APA-standard format

## Use Cases
1. Export of .RIS-file on a research project level (every document source is exported **once and only once** according to a predetermined schema)
2. Export of all incidents related to a research project and creation of foot-notes for text by outputting in a data format fitting for tabular data. 

## Reference types
References shall adhere to predetermined templates. 

1. Archival material
    * This reference type **must** contain a proper archival reference created through the Archival Batch Upload feature.
    * This is mirrored in the data-structure by the "Document" having an "Item" reference.
2. Other documents
    * This reference corresponds to individually added documents to the database.
    * This reference should be considered a catch-all to allow for sources that do not fit the standard archival model  
    (Journal articles, books, newspaper clippings etc)
    * The desired reference for these documents can be specified by the researcher in a specific field
    * If the researcher does not specify the output they desire a boilerplate output will be used: eg. <type>:<name>, (SourceID: XXX)

# Reference exports

## RIS.format feature

## Incident export feature

# Examples
