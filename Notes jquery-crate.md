# Notes jquery-crate

[Github](https://github.com/Chat-Wane/jquery-crate)

Represents one document  

***Important files:***

- **cratify.js**
- **model** - signaling.js and model.js
- **controller** - closebutton.js
- **view** - metadata.js, statesheader.js and link.js

## JS classes
  
**cratify function** *- cratify.js*:

- set options
- initialize MVC pattern
- optionnally join session


### Model

- **Signaling** *- signaling.js*:
	* socket
	* sharing
	* join

- **Model** *- model.js*:
	* gather all important data related to document sharing
	* what thing is crate-core ?!
		
- **GUID** *- guid.js*:
	* provides unique identifier	
	
### Controller
	
- **EditorController** *- editor.js*:
	* reacts to text addition/removal
	
- **CloseButton** *- closebutton.js*:
	* callback when a document is closed
	
- **Preview** *- preview.js*:
	* stylish view of the document
	* bind with button Preview in menubar

### View

- **Metadata** *- metadata.js*:
	* popup with sessions infos when hover crate icon
	
- **StatesHeader** *- statesheader.js*:
	* popup with network status (globe button in menu bar)
	* popup with signal status (when sharing, circle that rotates)	
- **CloseButton** *- closebutton.js*:
	* creates close button dom element

- **LinkView** *- link.js*:
	* bottom part with link for sharing	
	
- **Editor** *- editor.js*:
	* creates ace editor with options	

- **Preview** *- preview.js*:
	* just hide something
	
- **RoundButton** *- roundbutton.js*:
	* set style to menu bar buttons	
	
- **Structure** *- structure.js*:
	* css for header and document body