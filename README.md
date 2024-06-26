# RoughPad
A Handy Tcl/Tk Jotter for the Desktop

<img alt="RoughPad Logo" src="http://ideaware.stamatis.uk/wp-content/uploads/2015/12/RoughPad.png" width="48px" height="48px" />

## RoughPad - { Quick Note Manipulation }
RoughPad is a simple Tcl/Tk application for handling and manipulating text, useful for programming, web surfing, keeping program notes and generally anything that may otherwise require keeping a pen and writing pad handy. The interface is super-simple and self explanatory.

### { Program Options }
This program creates two objects:
- a resource file (_.RoughPadrc_)
- a storage directory (_.RoughPadStore_)

in the user's **$HOME**, for storing program preferences and notes respectively.

The program will save options and data on exit and restore them when it loads.

Appending the **-m** option when running the program will start it minimized in the taskbar.

Right-clicking in the text area brings up a context menu for text manipulation.

#### The "RoughPad" and "TempPad" tabs
The "RoughPad" is saved and restored automatically on closing and loading the program, respectively.  
The "TempPad", "ScrapPad", "AuxPad" and "WritePad" tabs function the same way as the "RoughPad" in the sense that their contents are preserved and restored upon program Exit / Start and you can still save its contents in a file similarly to the "RoughPad" via the context menu.

### { Program Setup }
This program is going to be installed by default in your **$HOME/bin** directory. If you have not set your **$HOME/bin** in the **$PATH**, see [this](http://istos.xyz/linux/include-homebin-in-any-desktop-environment/ "Include $HOME/bin in any Desktop Environment") or [this snippet](http://istos.xyz/linux/include-homebin-in-the-path-for-bash-shell "Setup your $HOME/bin in the $PATH") for details.

To run this program, you need to have the following packages installed in your system (Check with your package manager):

- _**tcl**_
- _**tk**_
- _**tklib**_
- Either _**tcl-signal**_ or _**tclx**_ (or both)

#### Once the above packages are installed
- Download your preferred variant (**_RoughPad-tclx_** or _**RoughPad-tcl-signal**_)
- Move the downloaded tarball into your **$HOME**, as all extracted files and directories will be relative to your **$HOME**
- Expand the tar file in a terminal by issuing:  
<code>**tar xf RoughPad\_&lt;variant&gt;_&lt;version&gt;.tar**</code>
- Invoke the program from the terminal, running:  
<code>**RoughPad &**</code>  
to ensure that it loads properly and no error messages are shown.

If everything has gone ok, you should be able to find the program in the _**Accessories**_ program group on your desktop manager.

### { File List }
The tarball contains these files (relative to the user's $HOME):
<pre>
bin/RoughPad
.icons/RoughPad.png
.local/share/applications/RoughPad.desktop
</pre>

### { Note }
There are two variants of the program to download, one is set to work with _**tcl-signal**_ and the other with _**tclx**_. Choose the variant you want to download depending on which of the above package (_tcl-signal_ or _tclx_) you already have (or are planning to install) on your system. The only differences in code in the two variants are as follows:

#### tcl-signal variant:
**#package require Tclx**  
**package require Signal**  

#### tclx variant:
**package require Tclx**  
**#package require Signal**

![image](https://github.com/stamatisxm/RoughPad/assets/12468393/3be00597-086f-446b-86b6-59abb115251b)
