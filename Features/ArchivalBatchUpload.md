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

The pop-up window shall require the user to select:

1. First: An Archive from a drop-down list of all existing archives  
    1. The user shall from this view be able to navigate to a sub-panel from which they  
        can add an archive to the Archive table  
2. Second: An Intermediate which corresponds to every part of the archival structure between  
    the physical archive and the physical archive unit (box, volume etc). Examples of this could  
    be sub-archives, series, sub-series and so on. Only intermediates created within that archive  
    shall be shown to the user when selecting the drop down.
    1.   The user shall from this view be able to navigate to a sub-panel from which they can add  
        an intermediate to the Intermediate table 
3. Third: A volume which corresponds to the physical unit of storage inside which the documents were  
    found. 
    1. The user shall from this view be able to navigate to a sub-panel from which they can add a  
        volume to the volume table
4. Upon selecting a correct sequence of archival units (Archive, Intermediate, Volume), the contents  
    of a reference field shall be revealed which shows the archival reference that the documents shall  
    inherit from the structure selected. Emphasize that this cannot be changed after upload.

The pop-up window shall contain a button with which to trigger the batch upload process. 

#### Exceptions

- If the user tries to upload before a correct archival structure has been selected  
    (Archive, intermediate, volume): Show an error message indicating that they need  
    adhere to the archival structure 

## Adding Archival entities

The user shall be informed when creating an  
    intermediate that they are expected to add all the information down to the

## Selecting archival structure

## Selecting folder to upload

## Batch import window

## Other actions

## Bugs 

## Scripts