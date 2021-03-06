Metadata can mean different things to different users.  We mean "information about the file that you are working with."  Most computer programmes capture the filetype, filename, size, creator, date created and date modified, but DataStage also makes it easy to capture information relevant to the researcher (e.g. "control run," "use for Figure 2") and to others who want to make sense of the data ("captured using equipment X, protocol Y").


**Automatically-captured metadata**

DataStage automatically captures the general file attributes:

* Created: when the file was first uploaded to the server, not necessarily when the data file itself was created.
* Filename: the name of the file itself.
* Last modified: the timestamp given by the computer from which the file is being read. DataStage will take the timestamp of the user's computer the first time the file is uploaded, but if users work with the file directly from the DataStage mapped drive and save it in the same location, the timestamp will come from the DataStage server.
* Type: "file" or "folder", assigned automatically by the DataStage server.
* Owner: user account in DataStage.  If "author" or other metadata is captured by the programme that created the file in the first place, this will not be kept in DataStage. "Ownership" of the file will be granted to whoever uploaded it into DataStage.
* Location: filepath to location on server
* Size


**Optional extra metadata**

The web interface also captures "extended attributes." These are not in [RDF](http://en.wikipedia.org/wiki/Resource_Description_Framework)format, so are not machine-readable (e.g. they cannot be indexed by web crawlers). However, users can see this metadata from the "index" screen in the DataStage web interface.

The DataStage web interface can capture:

* The title of the file (a free-text field): this is not the same as the filename, and can be used to add more information.  For example, Filename = Xcf23.11.csv but Title = crysallography data 23 Nov

* A description of the file (a free-text field): useful for further information, e.g. "reference dataset", "control - bad image quality", "file originally created by M Stefanos."


**Notes**

* When using DataStage as a mapped drive, users can only see the filename, not the Title or Description fields.

* If users adopt standard nomenclature, they can can use the information in the "title" and "description" fields to filter results.

* Users can add to, update, or remove the information in the "title" and "description" fields in the DataStage web interface at any time. This will overwrite the previous information, but will not affect the data within or the "version" or timestamp.



### DataStage and repositories

DataStage can package datasets for submission to any [SWORD-2](http://swordapp.org/sword-v2/)-compliant repository (e.g. [DataBank](http://www.dataflow.ox.ac.uk/index.php/databank/db-about)).  When users decide to submit a data package to a repository, the metadata profile changes.

DataBank (and many other repositories) will automatically capture file system attributes from DataStage:

* The "title" field from DataStage (the one entered manually online), which will be called the "label" in DataBank.
* The filename(s) and "description" fields from DataStage do not appear on the surface of the data package in DataBank, but this information is kept as "extended file attributes" within the zipped data package, which users can access via the "manifest.rdf" file in DataBank.
* The name of the research group, as used by DataStage.

DataBank also assigns:
* Created date (a timestamp given by the DataBank server, not the date the data was created)

Users can also specify:
* A unique identifier for the data package: if users attempt to submit a data package with an ID which has already been taken, DataBank will require them to rename the data package, or to accept it as another "version" of the same data package. The user can decide which of these is the correct action in each case. The closer this ID is to natural language, the more useful it will be to anyone searching the archive.

* Description for the data package: the description field for each file is kept alongside the file, zipped inside the data package.  Users need to add a new description for the data package as a whole.

* DataBank can handle a separate field for adding license information, but the DataStage upload interface does not allow you to add this information yet. We are working on this. In the meantime, users can use the Description field to hold their license information – but this is only temporary and we would recommend you get in touch with your archive administrator if you are planning to upload real data and need to include licensing information.