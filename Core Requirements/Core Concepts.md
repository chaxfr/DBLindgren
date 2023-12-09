# DB Lindgren Core Cross Table concepts

### UUID

* All tables  shall **ALWAYS** have a UUID on record level, including Join Tables
* This is to allow for merging of databases
* This value  shall **ALWAYS** be a calculated field using the "Get(UUID)" formula to ensure uniqueness

### Unique Identifier (UID-string)

* Important tables, defined as those that may create a distinct external reference, eg. "This document in the database", or "This person mentioned in the database", shall have sequential numbers to enable easy find operations.  
* Two fields shall exist on all such tables, sequential number and identifying string

#### Sequential number
* The sequential number field shall adhere to the naming syntax **UID_Tablename**
* The sequential number field shall use the >Serial Number: on creation< field option

#### Identifying string
* The identifying string field shall adhere to the naming syntax **UID_STRING_Tablename**
* This field shall be created from two concatenated values:
    * A table identifier prefix, schema explained below
    * The sequential number
* The values shall be concatenated as such: "prefix" + "sequential number" with no intervening spaces. Eg, A5, P100 correspond to Archive 5 and Person 100



#### Prefix Schema

1. A - Archive
2. M - Intermediate (Precedence of I given to Incident, M for Medial)
3. V - Volume
4. ~~D - Document~~ Document shall not be given a prefix, but D shall be protected as prefix in case that changes
5. P - Person
6. O - Organization
7. I - Incident

Note: Item table not included as it is not a valid reference target

#### Usage guidelines

* The sequential number shall when not 
* The UID-string shall always be present in any reference export refering to that table.  
***CORROLLARY: In order for a table to be eligible for export it must have a unique identifier***


### Selection string
This section to be decided. Alternate needs depending on UUIDs and Sequential numbers

* ~~The selection string syntax shall allow for some variability in construction, but the guidelines below should be considered best practice~~
* ~~The selection string should adhere to the syntax **SS_TableName**~~
* ~~The selection string should concatenate all traits necessary to identify a record from a pop-up list~~
* ~~In a usage scenario where the sequential number shall **NOT** be the selected value, the selection string should be the leading element~~

## Personal Keys

* The UUID defined above shall when possible be used as personal key.
* This is viable so long as the number of entries is ~<30.
    * This is because only Pop-up menus work well with hiding UUIDs
* For usability reasons sequential numbers shall be used as personal keys in relations between:
    * Entities:
        * Document
        * Person
        * Organization
        * Incident
    * The type of menu shall then be "Drop_down" with a sequential number as key identifier

* As personal key this name shall **ALWAYS** adhere to the syntax "PK_Tablename", regardless of calculation basis
    *   Should a need for distinction arise, the two keys (UUID and Sequential number) should be suffixed _UUID & _Number
* Personal keys shall **ALWAYS** be referenced in related tables by the syntax "FK_Tablename", that is, it keeps its original table name when referenced in another table to ensure legibility.  

