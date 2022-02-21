## Welcome to GEEDiT-TermPicks!

This code is a special version of the Google Earth Engine Digitisation Tool (GEEDiT; Lea, 2018; https://esurf.copernicus.org/articles/6/551/2018/) that has been created as part of the TermPicks project that aims to create and maintain the largest dataset of homogenised marine terminating glacier terminus positions from Greenland. GEEDiT-TermPicks provides a bespoke tool built in Google Earth Engine for users to generate new terminus data from satellite imagery that are consistent with existing TermPicks data, allowing for them to be seamlessly added to existing datasets and for suitable for submission to expand the dataset. The code for GEEDiT-TermPicks is based on code for GEEDiT v2 (https://github.com/jmlea16/GEEDiT). For more information on the TermPicks project and the data that currently exist within it, see Goliber et al., 2022 (https://tc.copernicus.org/preprints/tc-2021-311/). 

The full TermPicks dataset can be downloaded here: https://zenodo.org/record/5117931#.YhNqR9_P23A

Below provides a quick walkthrough of how to use GEEDiT-TermPicks.

### Getting started

The code for GEEDiT-TermPicks can be found here https://github.com/jmlea16/GEEDiT-TermPicksa or a direct link to the Google Earth Engine interface can be found at https://liverpoolgee.wordpress.com/geedit-termpicks/.

The code runs within Google Earth Engine's JavaScript API. When the code is accessed through the link on the LiverpoolGEE webpage, the welcome screen for the user interface should automatically appear as shown below:

![image](https://user-images.githubusercontent.com/40822976/154939963-053417a6-80b4-4489-9940-581a9d7285fb.png)

Here we see a map view of Greenland, with a series of blue dots indicating each glacier that exists within the TermPicks database. New terminus data can be digitised for a given glacier by first zooming into the location where the glacier of interest is located. In this example we will zoom into Kangiata Nunaata Sermia (KNS), SW Greenland.

![image](https://user-images.githubusercontent.com/40822976/154940896-4252bb26-fc9c-49ed-8278-bc28ea87730c.png)

In this image we see that blue dots are located over the main trunk of KNS and the glacier to the north (Akullersuup Sermia). Before starting digitisation, the options to select which imagery need to be viewed can be defined in the right hand panel, including date, cloud cover, and satellite platform. Once you have defined the options that you wish, you can go to the next step by clicking on/near the blue dot on the map that is located on the main trunk of KNS. This will bring up the next screen panel.

![image](https://user-images.githubusercontent.com/40822976/154941832-ec3968a4-4800-4ef9-8b6d-0e321ae34a5b.png)

On this screen you will see that the location marker for KNS changes to red, to indicate that this is the glacier that has been selected. At the bottom of the screen, text boxes are included to allow you to enter your name and email address. These are compulsory fields, as where data are submitted to TermPicks updates, this will allow appropriate acknowledgement of your contributions. If you are unfamiliar with the region and wish to double check that you have selected the correct glacier, you can click the 'View Glacier Info' button, which will bring up available information regarding the glacier name and identification numbers according to several different previously published inventories of Greenland's marine terminating glaciers (see below).

![image](https://user-images.githubusercontent.com/40822976/154942798-3bdbf828-eac7-4021-9cd0-3a3a1943c2dc.png)

If this is the correct glacier, then you can progress to visualising the imagery from which the termini can be digitised by clicking the 'Go to images' button. Otherwise, if you wish to select a different glacier you can click the 'Go back' button to return to the previous menu and begin the glacier selection process again.

### Digitising termini from imagery

After clicking the 'Go to images' button, GEEDiT TermPicks will collate all available imagery according to the visualisation options defined in the previous menu. If there is a lot of imagery, this may take up to a minute and a "page unresponsive" warning may appear. If this happens, just wait and the imagery will eventually load, also showing the GEEDiT TermPicks digitisation interface:

![image](https://user-images.githubusercontent.com/40822976/154944129-908f9b58-4638-49d7-985c-7590f69c042d.png)

As with the normal version of GEEDiT, digitisation of termini can be performed by zooming to where the desired level of detail is visible and directly clicking on the screen. Similar to GEEDiT v2, GEEDiT TermPicks makes use of Google Earth Engine's drawingTools functions to allow more rapid and flexible terminus digitisation than was possible using GEEDiT v1. Once you have started digitising a margin, the final vertex of the terminus can be digitised by double clicking.

### Editing margins
As the terminus is being digitised you will see that each vertex appears as a solid white dot, and the mid-points between vertices appear as semi-transparent dots. 

![image](https://user-images.githubusercontent.com/40822976/154944903-b1cd1ee7-228f-460d-a90f-e07bb0e2a9ef.png)

Once a terminus has been finished after double clicking to draw the final vertex these dots will disappear. However, if you with to edit the digitisation after this, this can be achieved by pressing the Escape key on your keyboard and using the cursor to select the margin that you wish to edit. The solid and semi-transparent dots will re-appear, and these can be edited by using the cursor to drag them to the desired location. Note that editing any of the semi-transparent dots will result in vertices being added to the terminus digitisation.

If you wish to delete the margin and re-digitise it, this can be done by selecting it as before and pressing the Delete key on your keyboard. To begin digitisation again, either select the line vector drawing box in the top left of the screen.

![image](https://user-images.githubusercontent.com/40822976/154946787-06fb7448-f569-492e-a0d8-8cefa95076d6.png)

### Comparing the current image to other images

Occasionally, it may be useful to compare the current image to other recent imagery to provide context for your digitisation. This can be easily done using the menu panel in the top left of the screen, where buttons allow the preceding and following image to be visualised (and subsequently removed.

![image](https://user-images.githubusercontent.com/40822976/154947229-2f9de262-cd6a-4df8-b878-c5eeddf47766.png)

To aide comparison between images, users may wish to toggle the transparency of the visualised images. This can be done by hovering the cursor over the 'Layers' menu in the top right of the screen, and changing the transparency of the visualised imagery using the associated slider bars.

![image](https://user-images.githubusercontent.com/40822976/154947554-d11e197d-d638-4fe0-8842-bd223746223e.png) ![image](https://user-images.githubusercontent.com/40822976/154947612-3384e503-62c0-4708-b2b9-0c158f0971a9.png)

On the layers menu, the current image (i.e. the image that you are digitising the terminus for) will always be the lowermost layer on this menu. Those who wish to use this option should take care to ensure that the image that they digitise the margin from is that image, and not preceding/following imagery. To guard against any mistakes related to this, it is suggested that the 'Remove added images' button on the top left menu panel is clicked before any digitisation is performed.

### Image Quality Flags
For some images, issues may arise that impact the quality of the digitisation that can be performed. To ensure data quality, these can be noted using the image quality flag checkboxes in the lower left of the screen.

![image](https://user-images.githubusercontent.com/40822976/154948824-44e8cedf-d7ab-4703-955d-14aa90f4c0b3.png)

These image quality flags are:
1. To note whether the quality of the margin digitisation has been impacted by cloud or shadow
2. To note whether the digitisation has been compared against other imagery (this is automatically checked if the preceding/following image is added to the screen by the user)
3. For Landsat 7 if the digitisation is impacted by the failure of the scan line corrector (SLC) mirror (this is automatically checked for all Landsat 7 images that are SLC-off)
4. To note if only part of the margin could be digitised from the image
5. To add any **short** user notes that will be appended in the digitisation metadata

### Moving between images
There are three different options for moving between images in GEEDiT TermPicks. The simplest can be done using the buttons in the panel in the lower right of the screen, either moving to the next image or previous image.

![image](https://user-images.githubusercontent.com/40822976/154949793-83ae92fd-04a0-42f9-942b-d249fdfc5abd.png)

However, if users wish to skip several images or move to the image that is closest in time to a user-defined date, this can be done by editing the text boxes in the panel in the top right of the screen.

![image](https://user-images.githubusercontent.com/40822976/154949997-6f7d299e-3375-420a-acca-ff267ebeb548.png)

To move to the image that is closest in time to a user-defined date, simply enter the date in _YYYY_MM_dd_ format, **making sure to use dashes as the date separator**. If other date separators are used then this will return an error. Users should also take care not to enter impossible dates (e.g. 2022-02-30). GEEDiT TermPicks will then find the temporally nearest available image available, and update the textbox to display the date of the image that has been visualised. Alternatively, to move to a given image number in the list available, users can edit the image number within the range 1 to _X_ (where _X_ is the highest image number indicated in the panel). In each case, once the date/image number has been entered, to visualise the image users should press the Enter key on their keyboard.

### Comparing current image to previously digitised margins
In some cases, it may be useful to review how much a terminus has changed between the current image and those that have been digitised previously in the current session. Where this is the case, users should hover their cursor over the geometry menu in the top left of the screen, and tick the checkbox of the margin they wish to visualise. All previously digitised margins will appear in blue, and the current margin will appear in black.

![image](https://user-images.githubusercontent.com/40822976/154951521-d091a77c-2fbd-4291-a3c7-733548462181.png) ![image](https://user-images.githubusercontent.com/40822976/154951564-3da821c7-e513-47f7-a293-ded537be3686.png)

Geometry layers will exist for every image that has been visualised, though layers where digitisations exist for will have _(1 line)_ in green associated with the geometry layer label (see figure above).

### Exporting terminus data
Once all termini have been digitised, the data can be exported to a user's Google Drive by first clicking on the Export button in the lower right of the screen. **Note that this by itself does not export data to Drive. A couple more steps are needed!**.

![image](https://user-images.githubusercontent.com/40822976/154952278-65e12da7-aa40-4f82-9838-1bdf9be35a07.png)

In order to export the data, users make sure the Export Tasks tab can be seen by using the cursor to drag it into view from the top of the map

![image](https://user-images.githubusercontent.com/40822976/154952704-79635152-23eb-40e4-8160-39101abdabde.png)

You will see that the Tasks tab in the top right of the screen is highlighted in orange. Click on this tab and click the blue Run button that is associated with the export task.

![image](https://user-images.githubusercontent.com/40822976/154952957-fcd3b31f-79f4-4722-9b83-463865cdd743.png)

The export task menu will then appear where the export name, file name that will appear in Drive and the file export format can be modified. Note that the default option for export is GeoJSON format, as this will preseve complete metadata names and can be easily imported into platforms such as QGIS, ArcGIS, and be read by multiple coding packages in an offline environment (e.g. Python, Matlab etc.). It is however possible to change the file export format to shapefiles, or CSV format if desired.

![image](https://user-images.githubusercontent.com/40822976/154953494-5fc690f6-2285-4e1d-b4f8-2c4b8dafc50b.png)

### Questions and support

If you have any questions about GEEDiT TermPicks, or notice any bugs, please contact James Lea (j.lea@liverpool.ac.uk)
