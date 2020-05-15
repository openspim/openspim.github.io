---
---
# Pre-processing of OpenSPIM data

The 11 multi-view time-points of a *Drosophila* embryogenesis time-lapse
[**downloaded**](Raw_data "wikilink") on the previous page are files
saved directly from the OpenSPIM plugin during acquisition as [OME
Tiffs](http://www.openmicroscopy.org/site/support/ome-model/ome-tiff/).
Unfortunately, the current SPIM registration plugins are not able to
open the files due to metadata conflicts.

*Note: This is hopefully a temporary situation which will be remedied in
the future and make the following pre-processing step obsolete. Please
realize that Fiji, OpenSPIM and OME are large Open Source projects that
need to communicate to make things like this work. Typically no-one is
directly paid for this type of work and everyone is busy with what they
are paid for doing. Nevertheless, it is our priority to make the
handling of OpenSPIM data in Fiji as smooth as possible*.

In order to use the OpenSPIM ome.tiff data in [Fiji](http://fiji.sc) we
need to save them as **regular tiffs**. We will take this as an
opportunity to introduce the powerful [ImageJ macro
language](http://fiji.sc/Introduction_into_Macro_Programming) that is
very suitable to achieve such tasks with minimal programming experience.
The following ImageJ macro was recorded in Fiji and edited in the
[Script Editor plugin](http://fiji.sc/Script_Editor).

``` java
for ( t = 0; t < 11; t++ )
{
    for ( a = 0; a <= 4; a++ )
    {
        open("/home/tomancak/Desktop/OpenSPIM_for_website/spim_TL" + IJ.pad(t, 2) +"_Angle" + a +".ome.tiff");
        saveAs("Tiff", "/home/tomancak/Desktop/OpenSPIM_for_website/tiffs/spim_TL" + IJ.pad(t, 2) +"_Angle" + a +".tif");
        close();
    }
}
```

![Screenshot of Fiji Script Editor with re-saving ImageJ
macro](Script_editor_screenshot.jpg
"Screenshot of Fiji Script Editor with re-saving ImageJ macro")

The outer loop increments the time-points (we use built in ImageJ zero
padding function *IJ.pad(t, 2)*), the inner loop increments the angle.
The macro opens an ome.tiff in a directory
*/home/tomancak/Desktop/OpenSPIM\_for\_website*, saves it in a
sub-directory *tiffs/* as *.tif* and closes the file.

*Note: On a Windows machine the directory path would like this :
C:\\\\home\\\\tomancak\\\\Desktop\\\\OpenSPIM\_for\_website\\\\*

The easiest way to run the macro is to launch the *Script Editor* plugin
(press letter **l** on the keyboard to launch Fiji [Command
Finder](http://fiji.sc/Using_the_Command_Launcher) and then type Script
Editor, then click on *RUN*). Paste the macro in the Script Editor.
Select ImageJ macro from Language menu - this will result in helpful
syntax highlighting. If necessary modify the numbers in the loops to
reflect the **input/output directory**, the number of time-points
(**t**) and angles (**a**) in your time series. Save the macro or simply
run it.

It is a macro, therefore it will show every image it opens temporarily
before saving and closing it. The downside of this is that the computer
cannot be used for anything else during that operation.

*Note: If you wish to run the plugin faster without showing the images,
add this command as first line to the macro:*

``` java
setBatchMode( true );
```

The end result of running the macro will be 55 new files (11 time-points
x 5 angles) in the directory *tiffs/*. These are regular tif files that
we can use for [**bead based registration**](Registration "wikilink") in
Fiji.

[Category:Software](Category:Software "wikilink")
[Category:Operation](Category:Operation "wikilink")
