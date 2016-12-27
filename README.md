# encfs-macfusion2
This is an updated version of the EncFS plugin for Macfusion by Tobias Haeberle (https://thenakedman.wordpress.com/encfs/), adapted to work with macOS 10.12 Sierra's fork of Macfusion by ElDeveloper (https://github.com/ElDeveloper/macfusion2).
## Build the plugin
Clone the project recursively:
```
$ git clone --recursive https://github.com/dbarelop/encfs-macfusion2
```
Open with Xcode and build the macfusion2 subproject. After that, copy or make a soft link of the resulting framework `MFCore.framework` (you can find its location by selecting MFCore.framework under the 'Products' group and clicking 'Show in Finder' with the right mouse button):
```
$ test -d ~/Library/Frameworks || mkdir ~/Library/Frameworks
$ ln -s $MFCORE_PATH ~/Library/Frameworks
```
Open with Xcode the main project and build the EncFS scheme. Under 'Products' there shoud be the plugin (EncFS.mfplugin).
## Install the plugin
The plugin file (EncFS.mfplugin) has to be copied to Macfusion's PlugIns directory (`/Library/Application Support/Macfusion/PlugIns` to make it available to all users or `~/Library/Application Support/Macfusion/PlugIns` only for the current user).
## Credit
Thanks to:
- [Tobias Haeberle](https://thenakedman.wordpress.com) for his EncFS plugin (https://thenakedman.wordpress.com/encfs/)
- [Michael Gorbach](https://github.com/mgorbach) for the Macfusion software (https://github.com/mgorbach/macfusion2)
- [Yoshiki Vázquez Baeza](https://github.com/ElDeveloper) for fixing Macfusion for macOS Sierra (https://github.com/ElDeveloper/macfusion2)
