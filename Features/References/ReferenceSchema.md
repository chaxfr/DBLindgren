# Reference Definition and Export
This document shall contain the requirements for a script exporting the references of the  
database as defined by the ReferenceSchema requirements. Consider the Reference Schema  
a product definition section and the Reference Export section the production process specification. One defines the desired output, the other the way this is achieved in the database paradigm.

## Reference Use Cases
1. Export of .RIS-file on a research project level (every document source is exported **once and only once** according to a predetermined schema)
2. Export of all incidents related to a research project and creation of foot-notes for text by outputting in a data format fitting for tabular data. 

# Reference Schema

* This document shall contain a definition for the schema used for references.
* It shall also define a schema for exporting all incidents tied to a research project into a table format.
* References shall adhere to predetermined templates. 

## Reference types

### Document Reference values

* A Document shall have a field called ParentVolumeReference
* A Document shall have a field called ExplicitReference
* A Document shall have a field called DocumentReference

### Document Reference Field population

* If the document is created through a batch upload the ParentVolumeReference field shall be populated from the Volume the document is uploaded to through the batch process. The VolumeReferenceCode field shall be copied into the ParentVolumeReference field.
    * Volume reference values for individual documents cannot be changed by the researcher post-upload, except on the Volume level. This then changes the reference of all documents tied to that Volume. 
* If the document is created by individual upload. The ParentVolumeReference field will be empty and cannot be populated post-upload.
* The Researcher can always, regardless of upload origin enter any value they wish into the ExplicitReference field.

## Document Reference 
* The DocumentReference field is a calculated field which adheres to the following precedence rules:
    * If there is a ParentVolumeReference, always use this
    * If there is no ParentVolumeReference, use the ExplicitReference.
    * If neither present, leave blank.
* If the DocumentReference field is blank, this shall not block neither RIS nor the Incident export feature.
    * Values for sources shall **never** be imputed except as described above in Reference Field Population. Either they are given on upload, or explicitly by researcher. It is the researcher's responsibility to provide correct information at the time of upload and/or before exporting.

NOTE: This means that the researcher cannot overwrite a reference inherited from the archival structure. Should they wish to have an ExplicitReference for a specific document the correct way is to upload it individually and write the ExplicitReference. This is to avoid ambiguity. A document either has an archival source or an explicit source. If in doubt, archival takes precedence.

# Reference exports

* The export features (.RIS & Incident) shall extract relevant values from different tables in the database. Using these the export features shall compile one file each. 
* A specific export feature shall be triggered through the click of a button on the Research Project table level. (The Research Project table is defined in the ResearchProject table requirements.)
* The Research Project is conceptually a group label for incidents, eg. Incidents have a many-many relationship with Research Project.

### Common reference export process start

* Starting from the Research Project level, both reference exports shall collect all Incidents which belong to a Research Project. By iterating over these incidents the scripts shall compile their output.

## .RIS-format export feature

The .RIS-format export feature (hereafter RIS-Export), shall create a valid .RIS file with separate entreies for all documents tied to a Research Project through Incidents. 

### Selection Criteria

* The RIS-Export shall receive a list of Incidents belonging to the Research Project
* The RIS-Export shall find all Documents that are attached to these Incidents.
    * A Document shall only appear once - no duplicates

### RIS-Export Common traits

* All references exported will have the Type (TY -) Aggregated Database in the .RIS format
* Primary Title (T1 -) shall consist of a concatenation of the fields "DocumentType: DocumentTitle"
* Database (DB - ) shall be hardcoded to "EHFF-online" for the MVP version
* If DocumentReference is not empty the Availability (AV -) will have the DocumentReference string
* Data Source (DS -) shall serve as a repository for the DocumentUID string.

### RIS-Export Detailed Schema
07/12-2023 Will have to be tested and decided in common after demo and subsequent meetings

## Incident export feature

* This table format shall contain text snippets useable for footnotes in an APA-standard format


