========================================================================
F4Menu for all v0.20 rc4
========================================================================
http://www.shanny.com.cn/

About F4Menu
--------------------------
As the name implies, F4Menu pops up a context menu upon pressing F4,
the user then chooses an appropriate editor for the selected file.
Certainly, it is also possible to run F4Menu in the background
without showing the menu and automatically open a file with its
associated editors.

F4Menu can be launched by any application, particularly it's suitable
for using as F4 Editor for Total Commander.

F4 is the shortcut key of Total Commander/TC for opening and editing
files, it invokes the specified editor to open the selected file.
Unfortunately, in TC only one editor can be assigned to F4, so it is
impossible to choose other editors for different file types, or to
select different editors for one specified file type. F4Menu is the
right tool to solve these problems.

Features
--------------------------
1. Press a single key and choose the best suited editor to open your
   file.
   
2. Use different editors to open different files at the same time.

3. Double press a single key to open files with default editor.

4. Selection menu supports drag-and-drop for easy reordering of items.

5. Easy to use and configure to meet your most challenging demands.

How to use
--------------------------

1. Launch Mode

  1.1 Execute directly
    a. Use space-separated filenames as parameter, the filename which 
       contains space should enclosed by quota. For example:
         F4Menu.exe "C:\a b.txt" D:\ab.txt
    b. Open configure dialog without parameter.

  1.2 Launched by TC
    Should set F4Menu.exe as F4 Editor of Total Commander in advance:
      TC Configuration -> Options -> Edit/View -> Editor for F4
    Then press F4 on a file in TC.

2. Run Mode

  2.1 Foreground mode
    Startup with the selection menu. By default, press F4 to run
    F4Menu in this way. However, it can be changed by:
      Popup Menu -> Settings -> Options -> Run Mode -> Foreground mode

    a. The first menu item is current file name, if it is shown as
       "*.xxx", that means there are several files with the same
       extension. Choose this item to open the files with the system
       associated program. This item is shown in grey if no program
       is associated.
    b. The second menu item is the default editor, which is used to
       open all unassociated files in background mode.
    c. Common editors are shown in bold if they are associated with
       the current file, and in grey if the path is invalid.

  2.2 Background mode
    Open the files directly without selection menu. By default, press
    ESC+F4 or CapsLock+F4 to run F4Menu in this way. It can also be
    changed by:
      Popup Menu -> Settings -> Options -> Run Mode -> Background mode

    a. Open the file with the first common matching editor. If there's
       no matching editor, the default editor is used.

3. Shortcuts
  3.1 On selection menu
    The following shortcuts only available on selection menu:
      Space - Open the file with the first common matching editor. If
              there's no matching editor, the default editor is used.
      Enter - Open the file with the selected editor.
      Ctrl+Enter - Associate and open the file with selected editor.

  3.2 Launch application
    The following shortcuts is only available for launching F4Menu:
      F4 - Launch application in foreground mode (by default)
      ESC+F4 / CapsLock+F4 - Launch application in background mode
      F4 (Double press) - Open files with default editor directly

4. Settings
  4.1 Editors Setting Dialog
    Set parameters for editors, open this dialog by executing F4Menu 
    directly or via:
      Popup Menu -> Settings

    a. Editor's path supports all system environment variables, such as
       "%ProgramFiles%", "SystemRoot", "COMMANDER_PATH", etc.
    b. Editor's path support relative path which relative to F4Menu path.
    c. The extension supports wildcard '*' and '?', the former is used
       to match any string, and the latter to match any single charactor.
    d. The extension is separated by comma (,)
    e. Drag & Drop list items to reorder them.
    f. Drag & Drop file and shortcut to this dialog to create new entries.

  4.2 Options Dialog
    Set options for application,  open this dialog by executing F4Menu 
    directly or via:
      Popup Menu -> Settings -> Options

    a. Set the popup position of selection menu, some options are available
       in TC only.
    b. Set maximum number of files for once open to avoid misoperation.
    c. Set launch key for foreground/background mode.

Installation
--------------------------
1. Download F4Menu.zip (39kB, Unicode) from http://www.shanny.com.cn.

2. System requirements: Windows NT/2000/XP/2003/Vista/2008,
   Total Commander 7.0 or above.

3. Unzip F4Menu to any folder.

4. If using F4Menu with Total Commander, please refer to "How to use 1.2"

Frequently Asked Questions
--------------------------
1. Is it possible to associate an editor with empty extension, such as
   "Makefile"?

A: Yes, just leave the extension field empty, for example, "txt,,"
   associates with "txt" and empty extension.

2. In the settings dialog, I removed the first line of editors, but the
   following lines did not go up, is it a bug of F4Menu?

A: No. The first line is the default editor, if the default editor is
   removed, this line will be empty, but F4Menu does not promote the
   next editor to be default. You can also drag-and-drop to sort 
   editors in the list.

3. Can F4Menu run VBScript or JScript?

A: Yes, just set wscript.exe as the editor and the script as parameter.

4. I selected several files in an archive, but F4Menu only opened one,
   is this a bug?

A: No. Actually, TC cannot open files in archive directly, it must
   unpack the files to a temporary folder before opening them.
   TC only unpacks the file under cursor instead of all selected files,
   so F4Menu can only open the one TC has unpacked.

5. Inside an archive, a "User abort!" message is shown while pressing
   ESC+F4 to launch F4Menu, why?

A: As mentioned in question 4, TC unpacks the file before opening it,
   during this time, ESC key may be treated as a command to abort,
   this triggers the message in question. In this case, you can use
   another shortcut key: CapsLock+F4 (depends on setting).

6. Is it possible to remove the default editor?

A: Sure, you can drag & drop it down the list or remove it in both
   the pop-up menu and the setting dialog box.

History
--------------------------
[+]added	[!]fixed	[*]changed
[2009-05-26	v0.20 rc4]
 ! Cannot work with open mode "1 - Open all files as a list" (thanks to byblo@tc)
 ! Shift+F4 does not work on TC 7.0x (thanks to sergeich28@tc)

[2009-05-25	v0.20 rc1]
 + Not restricted to TC use only, can used by any application, such as explorer
 + Support space-separated filenames as parameter
 + Double press F4 to open files with default editor (thanks to xuanqing@newsmth)
 + Press Caps+F4 to launch will not change CapsLock status
 ! Throughly solve "Cannot find file in Dir" issue
 ! Incompatible with Shift+F4 function of TC 7.50 (thanks to ehab@tc, matt123@newsmth)
 ! Double press F4 in TC may open file twice

[2008-01-06	v0.15 final]
 + Language: Korean (thanks to dis1hades2)
 ! Cannot open UNC file (thanks to SanskritFritz@tc)
 ! Made option dialog wider

[2007-10-02	v0.15rc1]
 + Language: Polish (thanks to dong@tc)
 + Ability to Drag&Drop file and shortcut to setting dialog to create
   new entries. (thanks to lancaster@DRL, icfu@tc)
 + Show editor path & param in tooltips (thanks to lancaster@DRL)
 + New selection menu position: right of current file/opposite panel/
   center window (thanks to sergeich28@tc, icfu@tc)
 + Editor support relative path  (thanks to redgiant@DRL)
 + Editor support start path (thanks to eaglesky@DRL, byblo@tc)
 + Can open all files while selected amount exceed the limitation
 + Add manifest file (thanks to SanskritFritz@tc)
 ! Cannot realize non-native unicode file name (partial resolved)
 ! Cannot open the file in an archive or FTP server
 ! Cannot set the "maximum number of open files" to larger than 16
 ! Cannot open the file in network neighbor (thanks to leepg)
 ! The entry of setting dialog may automatically move (thanks to icfu@tc)

[2007-09-23	v0.141]
 + Danish Readme (thanks to petermad)
 + Substitute current undefined language string by internal English string
 ! crashed when trying to open multiple files in an archive (Raymond@tc,
   petermad@tc)
 * Remove the mnemonic-prefix chars for "OK", "Cancel" in language files
   (thanks to icfu@tc)

[2007-09-22	v0.14]
 + Language: German (thanks to icfu@tc)
 + Language: Russian (thanks to bayarookie@tc)
 + Language: French (thanks to byblo@tc)
 + Language: Romanian (thanks to eugensyl@tc)
 + Language: Hungarian-magyar (thanks to SanskritFritz@tc)
 + Language: Spanish (thanks to dott@tc)
 + Treat leading char of menu item as an implicit mnemonic-prefix char,
   and its priority is lower than ampersand(&) mnemonic-prefix char. 
   (thanks to zhuangv@newsmth)
 + Ability to unselect opened files (thanks to TucknDar@tc)
 + Window option: normal/maximize/minimize (Fantast@DRL, byblo@tc)
 + Add new shortcuts for Setting listview: Del removes editor, Shift+Del
   removes editor without confirmation (thanks to icfu@tc)
 + Add version info in file property (thanks to roentgen@tc)
 ! The foreground color of InfoText is not consist with system. (thanks
   to icfu@tc)
 ! Cannot work in the invisble folder which protected by Universal Shield
   (thanks to Fantast@DRL)
 ! Append a stange terminating char for Language name (thanks to petermad@tc)
 ! In Danish, the initial language name is not consist with setting. (thanks
   to petermad@tc)
 ! In French, Selection menu appears at the position of the [Current file] &
   [Mouse cursor] are inverted. (thanks to byblo@tc)
 ! Crash when set Winrar as editor (thanks to roentgen@tc)
 * Revise english language file & readme (thanks to frank@newsmth)
 * Removed mnemonic-prefix char &A &O &S for selection menu in internal
   English language.

[2007-09-16	v0.13]
ATTENDTION!
In this verion, the format of ini file is changed.
Please run INI_to_v013.exe to update ini before starting F4Menu.

 + Highlights single file selected by F4, un-highlights it when F4Menu
   exits. (thanks to zhuangv@newsmth, xuanqing@newsmth)
 + Use FileDescription as default editor name. (thanks to nevermind@DRL)
 + Update ini format. (thanks to icfu@tc)
 + Add language file Danish.lng. (thanks to petermad)
 + Add language file Dutch.lng. (thanks to RolandD)
 ! Cannot work on the search result list.
 * The default ini file is renamed to F4Menu.ini.template, and use
   %programfiles% as initial path. (thanks to icfu@tc)
 * Use "MS Shell dlg 2" as default dialog font. (thanks to icfu@tc)
 * Remove three mnemonic-prefix chars from selection menu (&A, &S, &O).

[2007-09-15	v0.12]
 + Highlights single file selected by F4. (thanks to zhuangv@newsmth)
 + Open mode: Open each file separately / Open all file as a list.
   (thanks nevermind@DRL)
 + Selection menu position: Current file/Mouse cursor. (thanks to
   render@newsmth, zhuangv@newsmth)
 ! Cannot work on Vista/2008.

[2007-09-13	v0.11]
 ! F4Menu cannot work if file size displayed in dynamic mode.
   (thanks to BillGates@newsmth)

[2007-09-12	v0.1]
Initial release

License Agreement
--------------------------
F4Menu is a free software and is provided "as is" without warranty of any
kind, including, but not limited to, the implied warranties of
merchantability and fitness for a particular purpose. Should the program
prove defective, you assume the cost of all necessary servicing, repair
or correction. This program can be freely copied/distributed without
breaking distribution package integrity.

Author
--------------------------
Shao Shanny (PRC)
http://www.shanny.com.cn/
Shannycn@gmail.com
