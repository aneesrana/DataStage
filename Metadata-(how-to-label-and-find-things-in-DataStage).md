Metadata can mean different things to different users.  We mean "information about the file that you are working with."  Most computer programmes capture the filetype, filename, size, creator, date created and date modified, but DataStage also makes it easy to capture information relevant to the researcher (e.g. "control run," "use for Figure 2") and to others who want to make sense of the data ("captured using equipment X, protocol Y").

When you add a file to DataStage, DataStage automatically captures the general file attributes:

* Created (when the file was first uploaded to the server, not necessarily when the data file itself was created)
* Filename (i.e. what you called the file itself)
* Last modified (the timestamp given by the computer from which the file is being read. It will take the timestamp of your local computer the first time you upload the file, but if you work with the file directly from the DataStage mapped drive and save it in the same location, the timestamp will come from the DataStage server)
* Type (options are "file" or "folder." This is assigned by the DataStage server)
* Owner (automatic, according to the user account on DataStage)
* Location (filepath to location on server)
* Size

Note: if Author or other metadata is captured by the programme that created the file in the first place, this will not be kept in DataStage. "Ownership" of the file will be granted to whoever uploaded it into DataStage.

The web interface also captures "extended attributes." These are not in RDF, so are not machine-readable. However, you can browse these from the "index" screen in the DataStage web interface.

We can capture:

    the title of the dataset (an additional field you populate manually – this is not the same as the filename, and can be used to add more info, e.g. Filename = Xcf23.11.doc but Title = crysallography data 23 Nov)
    the "description" field, a free-text box which you can use to give further information, e.g. "reference dataset" or "control - bad image quality."

Notes:

    If you are using DataStage as a mapped drive, you can only see the filename, not the Title or Description fields.

    If you use standard nomenclature, you can use the information in "title" and "description" to filter results.

When you decide to submit a data package to DataBank, the metadata profile changes.

DataBank will automatically capture file system attributes from DataStage:

    The "title" field from DataStage (the one you entered manually online), which will be called the "label" in DataBank.
    The filename(s) and "description" fields from DataStage do not appear in the metadata for DataBank, but this information is kept as "extended file attributes" within the zipped data package, which you can access via the "manifest" link in DataBank
    The name of the research group, as used by DataStage

DataBank also assigns:

    Created date (a timestamp given by the DataBank server, not the date the data was created)

You specify:

    An ID which is a unique identifier: if you try to use an ID which has already been taken, DataBank will require you to rename it, or to accept it as another "version" of the same data package. The user can decide which of these is the correct action in each case. The closer this ID is to real words, the more useful it will be to anyone searching the archive.

    Description (the description field you entered in DataStage is kept inside the .zip file with its related files. You need to add a new description for the data package as a whole).

    DataBank can handle a separate field for adding license information, but the DataStage upload interface does not allow you to add this information yet. We will work on this. In the meantime, you can use the Description field to hold your license information – but this is only temporary and we would recommend you get in touch with your archive administrator if you are planning to upload real data and need to include licensing information.

The only metadata/annotation tool for DataStage is the web interface, where you can add a title and description, independent of the filename.

You can add to, update, or remove the information in the "title" and "description" fields in the DataStage web interface at any time. This will overwrite the previous information, but will not affect the data within or the "version" or timestamp.