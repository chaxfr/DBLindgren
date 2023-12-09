# Tests to perform on Batch Upload Feature

1. Save a testing copy of the database and perform test on this so you do not have to reset sequential numbers
2. Open testing copy and perform the following tests of the batch upload

## Create Archival Structure

- With no existing archive, intermediates, or volumes: 
    - Create an Archive and commit
    - Create an Intermediate and commit
    - Create a Volume and commit
    - Upload >1 pdf through batch process

### Test selection

- Use Create Archival structure several times to create:
    - 2 archives, with
    - 2 Intermediates, each and
    - 2 volumes each
- In main Batch Upload window, sequentially select new archives, new intermediates, new volumes
    - Ensure that lower level choices are erased and must be repicked when a higher level changes
    - Ensure the refcode changes every time
- Perform two separate uploads and ensure the documents get correct references

## UI edge case handling

### Main Batch Upload

- Try to create an intermediate with no archive selected
- Try to create a volume with no intermediate selected
- Try to upload without all three selected

### Archive/Intermediate/Volume

- For each sub-category try to commit without the correct inputs (name & ref code)


## Test Log

- 07/12/2023 - All tests completed

