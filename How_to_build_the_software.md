This page just explains how to build the software needed for OpenSPIM.
For an overview of the source code, please have a look at [this
page](Overview_of_the_source_code "wikilink").

# Obtaining the source code

## The easy way

<span style='color:red;'>First, make sure you have your camera driver
installed\!</span>

You first need to install [the newest Microsoft
SDK](http://msdn.microsoft.com/en-us/windows/desktop/aa904949) and then
[Microsoft Visual Studio
Express 2010](http://go.microsoft.com/?linkid=9709949) (see [this
link](#Why_Microsoft_Visual_C.2B.2B.3F "wikilink") to find out why).

<span style='color:red;'>**Note:** You **must** install the SDK
*first*.</span> Please see Micro-Manager's [build environment setup
instructions](http://micro-manager.org/wiki/Building_MM_on_Windows#Setting_up_the_required_tools%7CMicro-Manager's)
for details.

Download & run the [OpenSPIM development environment
installer](http://openspim.org/downloads/OpenSPIM-dev-env-20131025.exe)
(it is actually a self-extracting archive, you can use
[7-Zip](http://7-zip.org) to extract the
[archive](http://openspim.org/downloads/OpenSPIM-dev-env-20131025.7z)
instead if you feel uncomfortable with an installer).

This will set up everything you need and perform the initial build.

It will also install the *OpenSPIM Dev Env* shortcut on your desktop so
you can easily start the development environment again.

**Note:** this installer will clone and download additional packages, at
the time of writing totaling to about 450 megabyte. You have been
warned.

## Manually

<span style='color:red;'>First, make sure you have your camera driver
installed\!</span>

**Note:** this section is intended primarily to describe what the
[development environment installer](#The_easy_way "wikilink") does.
However, you are welcome to follow these steps, if you really must.

### You need Git

First of all, you need to make sure that you have the version control
software [Git](http://git-scm.com) installed. If in doubt, just install
[Git for Windows](http://msysgit.github.com/).

### Cloning the Micro-Manager and support sources

Wherever you like, e.g. in your home directory, call these commands:

1.  git clone <git://github.com/openspim/micromanager>
2.  git clone <git://github.com/openspim/3rdpartypublic>

### Install Microsoft Visual Studio

You need a copy of the Microsoft Visual Studio. Please follow the
instructions on the [µManager
Wiki](http://valelab.ucsf.edu/~MM/MMwiki/index.php/Building_MM_on_Windows).

### Setting JAVA\_HOME

<u>Make sure</u> that the environment variable *JAVA\_HOME* is set and
points to a valid JDK (you can add environment variables by
right-clicking on the "Start" menu button, choosing "Open Windows
Explorer", opening the context menu of "My Computer", selecting
"Properties" and in the "Advanced mode" click on the "Environment
variables" button. You need to restart the Visual Studio after adding
the environment variable).

# Building Micro-Manager

After installing [Visual C++
Express 2010](http://msdn.microsoft.com/en-us/express/future/bb421473),
start the development environment via the *OpenSPIM Dev Env* desktop
icon created by the development environment installer. Launch *Visual
Studio* by calling

`vcexpress.sh`

and then open the µManager project via
*File\>Open\>Project/Solution...*. The file to load is located in
*<development-environment>\\src\\micromanager* and is called
*micromanager.sln*.

Build all of the software by clicking on *Build\>Build Solution* or by
pressing the F7 key.

For full details, see the instructions on the [µManager
Wiki](http://valelab.ucsf.edu/~MM/MMwiki/index.php/Building_MM_on_Windows).

## Why Microsoft Visual C++?

There exists an alternative to Microsoft Visual C++ which is not only
free, but also Open Source: [GNU C++](http://gcc.gnu.org/).

Unfortunately, it is impossible to build µManager on Windows with the
GNU C++ compiler. The reason is that Microsoft Visual C++ uses an
Application Binary Interface (*ABI*) which predates, and is incompatible
with, the standard defined by the C++ consortium, but GNU C++ abides by
the standard. All of the shared libraries provided by vendors were
compiled for Microsoft Visual C++, though, so linking using GNU C++ is
impossible.

**Note:** even if µManager requires Microsoft Visual Studio, it is
sufficient to use [the Express
version](http://www.microsoft.com/visualstudio/eng/downloads), i.e. the
free-of-cost one.

# µManager scripting/plugins

One of the coolest things in µManager is the Beanshell Scripting
support. You can launch it through the *Tools\>Script Panel* menu item.
Those Beanshell scripts can interact with the GUI of µManager through
the global *gui* variable which is actually an instance of
*org.micromanager.MMStudioMainFrame*, and with the MMCore through the
global *mmc* variable which is an instance of *mmcorej.CMMCore* (the
binding to the C++ core).

When prototyping, it is best to start out with Beanshell scripts and
once things get polished enough, turn them into µManager plugins. Such
plugins are connected to the µManager application through the method
*setApp()* which must be implemented when implementing the
*org.micromanager.api.MMPlugin* interface. This method is passed an
instance of *org.micromanager.api.ScriptInterface* which has a method
*getMMCore()*. Unfortunately, it has no method to retrieve a reference
to the *MMStudioMainFrame*, but you can use the static method
*getInstance()* of said class to retrieve the singleton.

To provide ease of transition between scripting and plugin coding, we do
the following in the OpenSPIM plugin: we have two fields, unsurprisingly
called *mmc* and *gui*, which are initialized in the *setApp()* method.

# Debugging

See [the Frequently Asked Questions](FAQ#Debugging "wikilink").

# Further reading

[A birds-eye view of the OpenSPIM source
code](Overview_of_the_source_code "wikilink")

[Category:Software](Category:Software "wikilink")
