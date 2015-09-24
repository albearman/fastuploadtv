#Fast Upload TV 
#### For content editors who don't care where their files go, and developers who do
A Template Resource Input Filter for MODx Revolution 2.2+

------------------------------------

The Fast Upload TV input provides the simplest possible file upload experience for the end user, 
offering single-button file selection & uploading without the use of the MODx file manager. File save paths are 
set on the TV itself, so the content-editor doesn't have to worry about where to save to.

### Installation Instructions
1. Install `Fast Upload TV` from the control panel
2. Replace files `/core/components/fastuploadtv/`
3. Replace files `/assets/components/fastuploadtv/`
4. In the control panel tab `Elements` find plugins `FastUploadTV`
5. Click the `System events` mark the events `OnFileManagerUpload`, `OnWebPageInit` and save


### Input Configuration Options
While hiding many of these features from the Resource editor, Fast Upload TVs are very customisable! They 
work with any stream-based (filesystem) mediasource, can be saved to a custom path within the source, and optionally 
prefix a string to the filename in order to make maintainance and curation of uploaded files easier over time. 
You can even restrict file upload types by specifying required MIME types!

#### Placeholders
Both the file `Save Path` and `File Prefix` fields can be customised by editing the corresponding fields in 
the TV Input Options tab. Both options can be customized dynamically with several placeholders:

* `{r}`     - Resource ID
* `{p}`     - Resource Parent ID
* `{ra}`    - Resource Alias (IMPORTANT! Alias can not contain spetssivolov prohibited OS)
* `{pa}`    - Resource Parent Alias (IMPORTANT! Alias can not contain spetssivolov prohibited OS)
* `{t}`     - TemplateVar ID
* `{u}`     - User ID
* `{d}`     - Day of month
* `{m}`     - Month
* `{y}`     - Year
* `{rand}`  - Random string of 6 characters
* `{dt}`    - Date and time format Y-m-d-H-s
* `{time}`  - Time format timestamp
      
#### Advanced Save Path routing using Snippets
You can also specify a snippet that returns a path string for advanced routing by using the @SNIPPET prefix
e.g. `@SNIPPET myPathingSnippet`


#### Restricting file types using MIME
MIME types describe the type of file to be uploaded and relate to the file extension.
Multiple upload types can be specified using a comma-separated list.

e.g. `image/jpeg`, `image/png`, `application/pdf` 

A (mostly) full list can be found [here](http://webdesign.about.com/od/multimedia/a/mime-types-by-file-extension.htm).