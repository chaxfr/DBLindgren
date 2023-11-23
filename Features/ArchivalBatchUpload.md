# Archival Batch Upload Feature description

## Navigating to the batch upload

### **'Add to database'** button

On the main view of the database, Main layout, there shall be a button which moves the user  
to an Upload layout. From here they shall be able to access tools which allow them to add  
archival items by batch upload.

### **'Batch Upload Archival Items'** button

In the Upload layout there shall be a button that opens the Import Files Pop-Up layout from  
which the user will be able to set everything before uploading documents to ensure that  
they will have a correct archival structure attached.  

*Should the user wish to upload a document outside of an archival structure they will have  
to do this through a separate upload process for individual documents.*



## Selecting archival structure

The pop-up window shall require the user to select:

1. First: An Archive from a drop-down list of all existing archives  
    - The user shall from this view be able to navigate by button to a sub-panel from which they  
        can add an archive to the Archive table  

2. Second: An Intermediate which corresponds to every part of the archival structure between  
    the physical archive and the physical archive unit (box, volume etc). Examples of this could  
    be sub-archives, series, sub-series and so on. Only intermediates created within that archive  
    shall be shown to the user when selecting the drop down.

    -   The user shall from this view be able to navigate to a sub-panel from which they can add  
        an intermediate to the Intermediate table 
3. Third: A volume which corresponds to the physical unit of storage inside which the documents were  
    found. 

    - The user shall from this view be able to navigate to a sub-panel from which they can add a  
        volume to the volume table
4. Upon selecting a correct sequence of archival units (Archive, Intermediate, Volume), the contents  
    of a reference field shall be revealed which shows the archival reference that the documents shall  
    inherit from the structure selected. Emphasize that this cannot be changed after upload.


## Triggering the batch upload

The pop-up window shall contain a button with which to trigger the batch upload process. 

### Exceptions

- If the user clicks the upload button before a correct archival structure has been selected  
    (Archive, intermediate, volume): Show an error message indicating that they need  
    adhere to the archival structure 

## Adding Archival entities

### **'Add an Archive'** button and panel

By clicking a button next to the archival selection drop-down a new pop-up window called:  
"Add New Archive" shall open. 

- The window shall allow for the creation of new archives
- Archives require two fields to be filled in:
    1. Name of Archive
    2. Reference code (eg. /SE/RA/)
- By populating the required fields and commiting, a new archive in the Archive table shall be  
    created for the user
- On commiting the user shall be returned to the main "Batch Upload Archival Items" window and  
 the added archive shall be available for selection

### **'Add an Intermediate'** button and panel

By clicking a button next to the archival selection drop-down a new pop-up window called:  
"Add new Intermediate" shall open. The button shall require that the user has selected the archive 
in which they want to create the intermediate. 

The user shall be informed when creating an intermediate that they are expected  
to add all the information down to the individual volume. The abstract nature of the intermediate  
requires that this be added to the the panel where intermediate is added.

- The window shall allow for the creation of new Intermediates
- Intermediates require two fields to be filled in:
    1. Name of Archive
    2. Reference code between the archival and volume level (Sub-Archive/Series/Sub-Series)
- By populating the required fields and commiting, a new archive in the Archive table shall be  
    created for the user
- As not all archives have an intermediate level. There shall be an option to add a "None" to  
  both the name and archive reference which will ignore it for reference concatenation purposes.
- On commiting the user shall be returned to the main "Batch Upload Archival Items" window and  
 the added archive shall be available for selection

NOTE: Due to the decided architecture an intermediate string can be very very long. There is at  
the moment no way around this.

### **'Adding a Volume'** button and panel



## Selecting folder to upload

## Batch import window

## Other actions

## Bugs 

## Scripts