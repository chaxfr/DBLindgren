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
- On commiting the user shall be returned to the main "Batch Upload Archival Items" window
    - The added archive shall be selected in the "Batch Upload Archival Items" window Archive drop-down

### **'Add an Intermediate'** button and panel

By clicking a button next to the Intermediate selection drop-down a new pop-up window called:  
"Add new Intermediate" shall open. 
- The button shall require that the user has selected the archive 
in which they want to create the intermediate. 
- The value selected in the archive drop down shall be carried and set in the new pop-up window.  
    to ensure that the new Intermediate has a parent archive 

- The user shall through a visual aid be informed when creating an intermediate that they are expected  
to add all the information down to the individual volume. The abstract nature of the intermediate  
requires that this be added to the the panel where intermediate is added.

- The window shall allow for the creation of a new Intermediate
- Intermediates require two fields to be filled in:
    1. Name of Intermediate
    2. Reference code between the archival and volume level (Sub-Archive/Series/Sub-Series)
- By populating the required fields and committing, a new Intermediate in the Intermediate table shall be  
    created for the user
- On committing the user shall be returned to the main "Batch Upload Archival Items" window
- The added Intermediate shall be selected in the "Batch Upload Archival Items" window Intermediate drop-down

**NOTE:** Due to the decided architecture an intermediate string can be very very long. There is at  
the moment no way around this.

Though the Intermediate is required for database reasons. There is no guarantee that the archive as such will actually  
have any kind of Intermediate level. For instance, personal archives might just be a jumble of things. DBLindgren requires  
that you add an intermediate anyway. However, there shall be a suggested naming convention for "Intermediate Suppression".

#### "Intermediate Suppression" (Dec 2 NOT IMPLEMENTED)
- There shall be a combination of Intermediate Name and Intermediate Refcode that triggers Intermediate Suppression 
- Using this syntax shall ensure that the Intermediate level is not expressed in any reference code output
- There shall in the add an Intermediate pop-up windwed be a definition of this syntax and its implications

### **'Adding a Volume'** button and panel
By clicking a button next to the Volume selection drop-down a new pop-up window called:  
"Add new Volume" shall open. 
- The button shall require that the user has selected the archive and intermediate 
in which they want to create the volume. 
- The value selected in the Archive and Intermediate drop downs shall be carried and set in the new pop-up window.  
    to ensure that the new Volume has a parent Archive and Intermediate

- The user shall through a visual aid be informed when creating a volume that they are expected  
to only the information relevant for the distinction of the lowest level of archival collection.  
This corresponds to any physical item that contains the source material (eg. box, binder, drawer etc.)

- The window shall allow for the creation of a Volume
- Volumes require two fields to be filled in:
    1. Name of Volume (eg. {1, 2, 3}, or "1984-1985, or "Christmas cards")
    2. Reference code for the final level. This will determine the group string that batch uploaded Items  
        shall have
- By populating the required fields and committing, a new Volume in the Volume table shall be  
    created for the user
- On committing the user shall be returned to the main "Batch Upload Archival Items" window
- The added Volume shall be selected in the "Batch Upload Archival Items" window volume drop-down 


## Selecting folder to upload

## Batch import window

## Other actions

## Bugs 

## Scripts