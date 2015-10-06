# Notes CRATE
[Github](https://github.com/Chat-Wane/CRATE)

Website code, editor is in [**jquery-crate**](https://github.com/Chat-Wane/jquery-crate) project.

Important files: **index.html** and **adddocument.js** *(* ***justDoIt*** *function)*,  see also **modaladddocument.js**

## Page structure
- **menu-right-header**: 2 buttons in the top menubar (at right)
- **documents**: block which host editors
- **features**: 3 blocks which highlights crate features (above documents)

## JS classes
### Model
- **Model** *- model.js*: 
	* contains data for ***Features*** and ***VersionView*** classes

### Controller
- **Github** *- github.js*:
	* menu button callback which opens project Github page  		
- **AddDocument** *- adddocument.js*:
	* callback for "add a document" popup buttons
	* function ***justDoIt*** which creates a new document  

- **CSaveButton** *- savebutton.js*: 
	* save document localy (called by ***justDoIt*** for editor save button)

### View
- **Features** *- features.js*:
	* fill features (presentation) blocks  
	
- **VersionView** *- version.js*:
	* fill home icon popup with changelog  
	
- **RoundButton** *- roundbutton.js*:
	* button style for both buttons "add a document" and "contribute on GitHub" in the top menu (at right)  
- **ModalAddDocument** *- modaladddocument.js*:
	* modal popup which appears after clicking on "add a document" button in the top menubar
	* include action for some callbacks (callback declaration are in ***AddDocument***)
	* popup to confirm document creation  
	
- **Document** *- documents.js*: 
	* creates part of the editor structure (function used in ***justDoIt*** function)