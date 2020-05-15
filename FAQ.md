---
---
# Camera issues

## I get the error that a core property is read-only?

Please make sure to run an up-to-date installation (you can call the
updater via *Help\>Update Fiji*). There was a bug in the HamamatsuHam
driver that has been fixed in the meantime (many thanks to Patrick
Gregorio of Hamamatsu who helped us a lot to resolve this issue).

# Community

## How to share images?

We use [BitTorrent
Sync](http://labs.bittorrent.com/experiments/sync.html) to have a shared
directory of images and stuff. After installing BitTorrent Sync, you
will need to add a folder using this "secret":
*fUS9i4Ps/g+MLohUPun1rEfK8b0A+ABQitckZiONwPZK5BPm1N/wYg==*

## How to share scripts/macros?

The ideal way, of course, is to add a Wiki page to this Wiki. However,
if you want to work on a macro together with somebody else, the easiest
way is to use kind of a [shared
clipboard](http://demo.firepad.io/#openspim).

## How to report bugs

We have a [ticket system](http://openspim.org/tickets/). If you [add new
tickets](http://openspim.org/tickets/bug_report_page.php), please make
sure to

  - the category is *OpenSPIM*
  - assign the ticket to yourself if you intend to solve it
  - add a target version if you want the ticket to show up in the
    [roadmap](http://openspim.org/tickets/roadmap_page.php)
  - add a concise summary and additional useful information in the
    description
  - if you need this ticket to be visible only to the core developers of
    OpenSPIM, mark it as 'private'

Once you added a ticket, you might want to go back to it and make it a
child of a goal ticket in the *Relationship* box.

## Are there similar Open Access projects for life sciences?

[Yes\!](FAQ#Other_Open_Access_projects "wikilink")

# Software

## How do I autostart µManager when Fiji starts?

In Fiji, run the command *Plugins\>Macros\>Startup Macros...* and add
the following lines to the end:

`macro AutoRun {`  
`       run("Micro-Manager Studio");`  
`}`

## How do I autostart the OpenSPIM plugin when µManager starts up?

If you want the SPIM plugin to be called everytime when Micro-Manager
starts, add the following lines to the *Fiji.app/MMStartup.bsh* file:

`setAccessibility(true);`  
  
`import org.micromanager.MMStudioMainFrame.PluginItem;`  
`for (PluginItem plugin : gui.plugins_)`  
`        if (plugin.className.equals("SPIMAcquisition")) {`  
`                plugin.instantiate();`  
`                plugin.plugin.show();`  
`        }`

## How do I start µManager from the command-line?

There are two ways, really. The Fiji way:

`fiji-win32 --run Micro-Manager_Studio`

Call the Studio directly, without first starting ImageJ:

`fiji-win32 --main-class=org.micromanager.MMStudioMainFrame`

## Can I run OpenSPIM with Windows 7 or 8?

At the time of writing, we know that the Hammamatsu camera works with
both Windows XP and Windows 7 using the [DCAM
driver](http://www.dcamapi.com/).

## How can I build the OpenSPIM software myself?

Please have a look at [this
page](How_to_build_the_software#The_easy_way "wikilink").

## Micro-Manager runs and loads my configuration, but the OpenSPIM plugin won't start, what should I do?

Try zeroing the positions of all the stages, especially the twister. You
can do this either by opening the Picard software (USB 4D-Stage Version
1.0) and clicking "All Home" and also "Set Zero" for the twister, or you
can do it in Micro-Manager by doing the following:

\- Launch Micro-Manager. - Click Tools -\> Script Panel. - Type or
copy/paste the following (If you did not use the default twister name,
be sure to replace the text in the line below with the correct name.):

mmc.setPosition("Picard Twister", 0);

\- Press enter.

If this doesn't correct the problem, repeat for the X, Y, and Z stages.

# Debugging

## Look at the CoreLog

Whatever you do, first have a look at the file CoreLog<date>.txt,
located in Fiji.app/ or whatever directory Micro-Manager was started in.

## When Micro-Manager does not list the driver

1.  Make sure the .dll is present in *bin\_Win32/mm/Win32/*
2.  If you copied the driver from an independent micro-manager
    installation, make sure the micromanager version the driver comes
    from corresponds to version embedded into OpenSpim.
3.  Use the [Dependency Walker](http://www.dependencywalker.com/) to
    detect missing dependencies

## The driver for my hardware is not listed in OpenSPIM, but it supported by micro-manager

In *theory* any hardware supported by micro-manager should work in
OpenSPIM. If the driver for your hardware is not listed in OpenSPIM, you
can add it to the OpenSPIM driver list by copying the *.dll* to the
*/mm/Win32/* folder. Watch out that the versions of micro-manager from
which the drivers originates and the version of OpenSPIM your are using
are compatible. For instance, OpenSPIM-20130131 is built on
[micro-manager
v1.4.9](http://valelab.ucsf.edu/~MM/MMwiki/index.php/Micro-Manager_Version_Archive)

## Micro-Manager just crashes when I connect <device>

Micro-Manager's memory management is not very safe on the driver side.
Try to start Fiji with less memory reserved for Java, e.g. *--mem=512m*.

If that does not help, try to find out what's in [the core
log](#Look_at_the_CoreLog "wikilink"), and if that fails, too, you might
have more luck [\#Using Visual Studio's interactive
debugger](#Using_Visual_Studio's_interactive_debugger "wikilink").

## Using Visual Studio's interactive debugger

Start Fiji, and before starting Micro-Manager use Visual Studio's
*Debug\>Attach to Process...* to attach to the process. After that, you
may set breakpoints (optional) and then start Micro-Manager in Fiji.

## Using Eclipse to debug MicroManager/SPIM Acquisition

### Option 1: Eclipse-only

1.  Make sure you have [Eclipse](http://www.eclipse.org/) installed.
2.  Add Fiji's JRE to Eclipse:
    1.  Window -\> Preferences; under Java, select Installed JREs and
        click Add...
        1.  Use Standard VM.
        2.  Set the JRE Home to *Fiji.app/java/win32/jdk1.6.0\_24* (or
            similar). Eclipse should fill in the rest.
        3.  Click Finish.
    2.  Check the checkbox next to the newly-added JRE.
3.  Create a new project for Micro-Manager Studio:
    1.  File -\> New -\> Java Project...
        1.  Uncheck "Use Default Location"
        2.  Point Location to */src/fiji/3rdparty/micromanager/mmstudio*
        3.  Eclipse should auto-configure all sorts of useful things.
    2.  Click Next.
        1.  On the Libraries tab, click Add External JARs...
            1.  From */src/fiji/3rdparty/bin\_Win32/jars/*:
                  - bsh.jar
                  - commons-math-2.0.jar
                  - ij-<version>.jar
                  - MMCoreJ.jar
                  - MMAcqEngine.jar
                  - swing-layout-1.0.4.jar
                  - swingx-0.9.5.jar
    3.  Click Finish.
4.  Create a project for SPIMAcquisition:
    1.  File -\> New -\> Java Project...
        1.  Uncheck "Use Default Location"
        2.  Point Location to
            */src/fiji/3rdparty/micromanager/plugins/SPIMAcquisition/src/main/java*
        3.  Let Eclipse auto-configure things.
    2.  Click Next.
        1.  On the Projects tab, click Add... and select the mmstudio
            project added above.
        2.  On the Libraries tab, click Add External JARs...
            1.  From */src/fiji/3rdparty/bin\_Win32/jars/*:
                  - ij-<version>.jar
                  - MMCoreJ.jar
    3.  Click Finish.
5.  Depending on your workspace settings, you may need to reduce the
    enforced JRE level for both projects:
    1.  Right click on each project and go to Properties.
    2.  Select Java Compiler.
    3.  Enable project-specific settings and set the Compiler Compliance
        Level to 1.6 (depending on the JDK used by Fiji).
    4.  Click Apply then OK.
6.  Set up the debug configuration:
    1.  Run -\> Debug Configurations...
        1.  Create a fresh launch configuration
        2.  Use SPIMAcquisition as the project.
        3.  For the Main class, click *Search...* and find *ij.ImageJ*
        4.  On the Arguments tab, under VM arguments, pass the
            following:
            `-Dplugin.dir=fiji/3rdparty/micromanager/bin_Win32`
            (modifying as appropriate).
        5.  On the Classpath tab, select SPIMAcquisition, then Add
            External JARs...
            1.  From fiji/3rdparty/micromanager/bin\_Win32/jars:
                  - MMAcqEngine.jar
        6.  Click Apply.
    2.  Click Debug to make sure everything works.

### Option 2: Eclipse and Maven

1.  Follow steps 1-3 above. Additionally install
    [m2e](http://eclipse.org/m2e/) for Maven support in Eclipse .
2.  Import the SPIMAcquisition Maven project
    1.  File -\> Import...
    2.  Select Maven -\> Existing Maven projects
    3.  Browse to *micromanager/plugins/SPIMAcquisition* and let m2e
        work.
    4.  Click Finish
3.  Continue on steps 5 and 6 above.
