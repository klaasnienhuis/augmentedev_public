# Augment 3D model publisher for 3ds Max 2012 and 2013
This project consists of a publisher to [Augmentedev] (https://www.augmentedev.com) for 3D models made in [3dsMax] (http://usa.autodesk.com/3ds-max/).

# Documentation
The Augment 3D model publisher exports your 3D models directly from 3dsMax to your online account at Augment. The publisher takes away all the manual settings, zipfiles, filepaths and uploading. Optionally the publisher also lightbakes your 3D model. This enables you to present your models in the best light possible with minimal effort.
To publish a model you need a 3D model, an API-key and a title. The 3D model you provide yourself as well as a title. The API-key you can get on your profile-page in your Augment account. You can also provide optional information like a weblink, a product ID if relevant, a description and some keywords. All of these items can also be added, deleted or changed from your online Augment account.
##Installing the script
The script comes as an .mzp file. This is a self-extracting file specifically made for 3dsMax. You can either drop the file on one of the viewports or run it by going into the main menu > maxscript > run script. After doing either of these, you'll get a dialog which tells you how you can add the script to your interface. You can add it as an icon on a toolbar, give it a keyboard shortcut or add it to a menu or quad. If you've added it as an icon to a toolbar for instance, you then just click the icon to run the script.
Check out this blog-article by Klaas Nienhuis on the process. It uses another script but the procedure it the same.
##First use
When you first run the script, it will ask you to enter an API key. You can click on the link in the dialog to go to your account page. After entering your API key, the script will remember it and won't bother you again. The API key is the key to your account. 
##Overview
Open the script in 3dsMax 2012 or 2013, enter a title in the script interface, select the models you want to publish and press the big red button "Make an export for Augment". The script will now perform some actions for you:
*save the selected objects to a new file
*open the new file
*add a light (sun and sky) and a camera matching your renderengine (scanline, mentalray and vray supported)
*unwrap the objects
*lightbake the objects
*make a screengrab with the baked textures
*export the objects
*send the exported file with the textures, screengrab and the data from the script to Augment

It will show progressbars and messages and the interface will be unresponsive as some of the tasks involve setting up the viewports and object selections.
When uploading has finished, the script shows a popup with a weblink to the model you can share and a QR-code you can scan with the augment-app to view the model. You need to have the printed marker to view the model on your device.
##Files
The script saves the selected objects to a new file. Before opening that file, t will ask you if you want to save the current file. Always wake sure you have a backup of the files you're working with.
##Geometry
The script can only process real geometry. Proxy or xref objects, points, helpers and shapes can't be unwrapped, baked or exported. Make sure that everything you want to export is actually real geometry present in your scene. To make sure it is you can try to convert the objects you want to export to poly or mesh.
Although the Augment engine is pretty powerful, it's always a good practice to optimize your model. Remove pieces of your model you'll never see on a mobile device. For instance the inside or interior of objects or tiny objects. If an object is tiny and irrelevant to the overall experience depends on the size of the main object. If you're going to publish a microwave, the keys on the keypad are probably important. If you're going to publish an entire kitchen, the keys on the microwave probably are less important. 
##Textures
All textures normally are going to be lightbaked. This means the renderer needs to know where all the original textures are the models are using. Check in the asset manager that the textures are present in the location where it says they are. Seeing the textures in your viewport doesn't mean the renderer can actually find them. To fix this you can use another script dealing with external filepaths such as "Relink bitmaps" by Colin Senner.
##Lightbaking
The script will lightbake every single object you select. You can pick the mapsize in the script. It will use the same mapsize for every object. If you have many objects rendertimes will be longer than if there is only one object. If the sizes or surface areas of the different objects in your scene differ greatly, the objects will also have lightbaked textures with varying resolutions. We're advising to try to keep the objects about the same size. You can do this by combining or splitting objects. 
##Conclusion
So basically the script does a lot of work for you when lightbaking a model and publishing it to Augment. However it won't solve issues with the model which can't be automated such as deciding which object is important and which isn't or find textures for you which aren't there. Some expertise is still needed to make a successful export.

More tutorials and articles on [klaasnienhuis.nl] (http://www.klaasnienhuis.nl)

## License

## Warranty

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.

Happy publishing!
klaas Nienhuis

