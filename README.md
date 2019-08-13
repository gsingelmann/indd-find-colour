# Find Colour in Everything

An InDesign Script to mark all occurances of a swatch in the open document.

## Using the Script

1. Make sure you’ve got a document open
1. Double-click the script in the Scripts panel.
1. Select the colour you are looking for.
1. Look at all the red rectangles :)
1. Either undo (cmd-Z) or delete the layer "gefundene Farbe"

![select color](./pix/01-panel.jpg)

![the result](./pix/02-reds.jpg)

## Installation

### Basic Installation

1. Open the Scripting Panel

![panel](https://www.cuppascript.com/stuff/readme_pix/install/01-menu.jpg)

2. Right-click the entry "User" and select "Reveal in Finder".

![reveal folder](https://www.cuppascript.com/stuff/readme_pix/install/02-reveal.jpg)

3. Place script in folder "Scripts Panel"

![reveal folder](https://www.cuppascript.com/stuff/readme_pix/install/03-folder.jpg)

### Startup Scripts

Some scripts are declared as "Startup Scripts". These are scripts that are automatically run, right after InDesign starts.

For those simply create a folder with the name "Startup Scripts" right beside the "Scripts Panel" folder and place the script inside.

### Storing scripts somewhere else

The "Scripts Panel" folder is located in preferences folder of your current InDesign-Version.

I have installed several versions of InDesign (since the customer and his version is "always right" ;) ) but I want to have a single installation folder that is shared among the InDesign-versions.

It used to be that an alias was good enough for this purpose but that changed a few years ago. Now you need something that is called a [symbolic link](https://apple.stackexchange.com/questions/115646/how-can-i-create-a-symbolic-link-in-terminal).

1. Find the Terminal in Application:Utilities:
1. Open the folder that contains the folder where you want to store your scripts
1. Drag the folder-symbol in the window bar onto the Terminal

![open folder in terminal](https://www.cuppascript.com/stuff/readme_pix/install/04-open-terminal.jpg)

By dragging the folder onto the terminal that folder is automatically set as 'current folder' so you don’t have to bother about paths.

4. Now type `ln -s nameofsourcefolder nameofsymboliclink`

In my example: 

``` bash
ln -s my\ real\ scripts\ folder/ my-scripts
```

![symbolic link](https://www.cuppascript.com/stuff/readme_pix/install/05-link.jpg)

5. Drag the link (here: `my-scripts`) into your "Scripts Panel" folder

### Folder Structure

Instead of simply putting all your scripts flat into the Scripts Panel you can create a folder structure.

![folders](https://www.cuppascript.com/stuff/readme_pix/install/06-structure.jpg)

The Scripts panel will show the same structure:

![folders](https://www.cuppascript.com/stuff/readme_pix/install/07-panel.jpg)

