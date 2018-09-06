[Working commands](WorkingCommands.html) --- MISSING

 Unicode Build:

-   (1.0.48.873) (21/10/10) Tried to improve performance for
    iniread/iniwrite. If using the simpleini-routines 200 entries lasts
    one minute. If using TextFile which can read non-/ and unicode files
    it lasts 4 minutes. Fixed URLDownloadToFile.
-   (1.0.48.760) (14/10/10) Fixed endless loop for command INIREAD if
    the file to read does not exist
-   (1.0.48.754) (13/10/10) Fixed Send, but still work left. Unicode and
    characters can be sent. Just english keyboard settings sends the
    correct data
-   (1.0.48.645) (09/09/10) Changed send to support unicode / send, {ASC
    xxx} is now sending unicode chars
-   (1.0.48.616) (05/09/10) Fixes ControlSend
-   (1.0.48.598) (03/09/10) Added new command "RunAt" (specific time or
    event)
-   (1.0.48.583) (03/09/10) Fixed \#include. A\_OSType & version =
    WIN\_CE
-   (1.0.48.473) (28/07/10) Fixed reading unicode scripts. Changed
    parsing the run command parameters.
-   (1.0.48.372) (19/06/10) Added new command to rotate the screen
    (ChangeDisplaySettings)
-   (1.0.48.300) (26/05/10) Fixed RunWait
-   (1.0.48.291 ) (25/50/10) Fixed memory leaks in RegRead / RegWrite
    functions
-   (1.0.48.285) (25/05/10) Fixed  Binary Data. /
-   (1.0.48.250) (11/05/10) Fixed FileSetTime. Changed CreateFile
    parameters. // Fixed test script // Fixed Ceil // Fixed IniRead
    IniWrite IniDelete
-   (1.0.48.239) (10/05/05) Changed a lot of functions to allocate less
    stack space (TCHAR[10000]-\> new...) / Fixed compiler warnings /
    Fixes code analysis
-   (1.0.48.124) Fixed bug in compiled scripts
-   (1.0.48.119) The compiler is now using unicode. Before that change
    the script is appended to the exe as ansi. Now the appended script
    is unicode, too. Compiler can change the ahk-icon now.
-   (1.0.48.56) Fixed DllCall, DriveGet, Edit, WINCEUtil\_Run (internal)
-   (V3) Fixed ControlGetFocus.
-   (V2) Fixed reading long files. Fixed Peekmessage (needs
    CONFIG\_WINCE being defined)
-   (V1) Just compileable. Erased the working commands list. Testing
    each function from the beginning



* * * * *


 (old ansi version)


-   (v1) FileAppend MsgBox
-   (V3) FileCopy, If, If between, if in, if contains, ifequal,
    ifgreater, ifinstring, ifless, ifwinactive, ifwinexist, Pause,
    return, loop, break, else, Expressions (a:=3 / b:= a\*4), Gosub,
    Goto
-   (v4) a\_ahkPath a\_ahkversion a\_workingdir a\_scriptdir
    a\_scriptname a\_scriptfullpath a\_linenumber a\_linefile
    a\_thisfunc a\_thislabel a\_ahkversion a\_ahkpath a\_exitreason(?)
    a\_YYYY A\_MM A\_DD a\_MMMM a\_MMM a\_DDDD a\_DDD a\_Wday a\_yday
    a\_yweek a\_hour a\_min a\_sec a\_msec a\_now a\_nowutc a\_tickcount
    A\_IsSuspended A\_BatchLines A\_TitleMatchMode
    A\_TitleMatchModeSpeed A\_DetectHiddenWindows A\_DetectHiddenText
    A\_AutoTrim A\_StringCaseSense A\_FormatInteger A\_FormatFloat
    A\_KeyDelay A\_WinDelay A\_ControlDelay A\_MouseDelay
    A\_DefaultMouseSpeed A\_Temp \~A\_OSType \~A\_OSVersion A\_Language
    A\_ComputerName A\_WinDir A\_UserName VarSetCapacity functions
    Labels Continue
-   (v5) A\_ProgramFiles ProgramFiles A\_Desktop A\_StartMenu
    A\_Programs A\_Startup A\_MyDocuments A\_ScreenWidth A\_ScreenHeight
    ExitApp abs() FileExist() InStr() SubStr() StrLen() asc() chr()
    IsLabel() exp() Ceil() Floor() log() ln() mod() round() sqrt() sin()
    EnvAdd EnvSub is(float int, time...) Arrays FileGetAttrib Autotrim
    if.between
-   (v6) Gui: Button, Text, Label, ComboBox; FileSetAttrib FileGetAttrib
    FileGetTime FileSetTime IfExist IfNotExist StringGetPos SetFormat
    FileCreateDir FileRemoveDir FormatTime DriveSpaceFree
-   (v7) RegRead RegWrite FileRead FileReadLine InputBox ErrorLevel
    Loop(files & folders) Loop(read file contents) Loop(parse a string)
    Loop(registry)
     FileCreateShortcut (only Target and Shortcutfile are supported)
     FileGetShortcut (Only OutTarget and OutDir are supported)
     ListLines ListVars IfMsgBox SetTimer Sleep Sort
-   ( v8 ) Transform
-   (v9) Gui, Add (5%)
-   (v10) IfWinExist WinActive WinExist WinActivate MouseClick
    Process(Exist) Run Send
-   (v11) ControlGetText ControlGetFocus ControlFocus ControlSetText.
    Removed OS-dependencies, so AutohotkeyCE is working on PNA or other
    WinCE "lite" devices. StringGetPos / InStr() StringLeft StringLen /
    StrLen() StringLower StringMid / SubStr() StringReplace StringRight
    StringSplit StringTrimLeft StringTrimRight StringUpper 
-   (v12) WinClose WinGetActiveStats WinGetActiveTitle WinGet(ID,
    IDLast, PID, ProcessName, Count, List, MinMax, ControlList, Style,
    ExStyle) WinGetClass WinGetPos WinGetText WinGetTitle WinHide
    WinKill WinSetTitle WinSet(bottom, top, disable, enable, redraw?)
    WinWait WinWaitActive 
-   (v13) WinMove ControlGetPos WinWaitNotActive WinWaitClose
    FileCopyDir Process(Close, Wait), After you have registered the
    ahk-extension (with the 2 lines script above) you can start any
    ahk-file.
     Control: Check Uncheck Enable Disable Show Hide ShowDropDown
    HideDropDown
     FileDelete FileMoveDir ControlClick ControlMove SoundPlay SplitPath
    Random FileRemoveDir FileGetSize FileGetTime FileMove FileGetVersion
    SetTitleMatchMode CoordMode SetBatchLines StringCaseSense
-   (v14) reload command.
     Starting a new instance of a thread kills the current one. This is
    working now. 
-   (v15) Clipboard functions. This was tricky, because the clipboard is
    unicode, but the ahk-variables are not. The locked clipboard-buffer
    is being returned and filled by ahk functions. If you try to write
    that chars the clipboard isn't able to handle this. The conversion
    has to be done by hand.
     Listview \<-\> Gui,Submit: conversion between unicode and char
    corrected. 
     loop, \\path\\\*.\*, x, x fixed 
-   (v16) Clipboard functions Part2. When transfering huge strings
    from/to clipboard, the application crashes (stack overflow), so I
    had to rewrite these parts of the code
-   (v17) things like send, {LWin Down}{vkc2sc065}{LWin up} are starting
    to work. (7%)
-   (v18) Listview is working with longer texts than 128 bytes
-   (v19) FileSelectFile
-   (v20) menu + menu, tray: since (AFAIK) there's no "right mouse
    click" on a PDA, I'm using just the left click.Edit: Tap and hold
    must work to create a context menu
-   (V21) fixed GetText of comboboxes, inputbox
-   (V22) migrated code to AHK 1.0.48. Wish: rotate screens: Worked in
    emulator by using

  -----------
  **Code:**
  -----------

-   (V23) Listview: Report view mode is working. Context menu is shown
    at the right lower corner now.
-   (V24) RegExMatch / RegExReplace
-   (V25) Gui, add, Picture is able to load a bitmap. Gui, Add, Picture,
    x1 y30 w100 h100, %a\_scriptdir%\\AHK2008.bmp
     Thanks to Berry who has done the following things: 
     - Fix: BIV\_ScriptFullPath and beep.
     - New: Full support for INI-commands by using open source code.
    (Read, Write, Delete).
-   (V26) RegWrite / RegRead / RegDelete /
     Soundplay (standard system sounds \*-1 \*16 ...) 
     Shutdown (reboot + suspend)
-   (V27) ControlGet, List, ComboBox + ListBox + SysListview / LV\_ADD /
    LV\_ModifyCol / -Multi / NoSortHdr/ a\_gui / A\_GuiWidth
    A\_GuiHeight /
     Fix: ListLines / A\_GUIControl / A\_IsAdmin (=true) /
     Fix: context menu :Edit script
-   (V28) Reorganized the whole project structure. You can build
    debug/release for CE/win32 and the compiler
     The compiler is working now on ce devices. Updated the installer.
-   (V29) Fixed Control, Add, x, ListBox / Fixed Control, EditPaste /
    Added Tap&Hold / Fixed EnumChildFind so finding a window with a
    window text is working now. /
     Fixed Gui, Add, CheckBox / Fixed Gui, Add, Radio / Fixed Gui, Add,
    DateTime + ListView + TreeView (width)
     Fixed LV\_Add (only first column was set correctly) / Fixed
    ControlGet, var, LINE
-   (V30) Fixed Click / Checked CoordMode / Fixed DriveGet Capacity /
    Fixed Edit / Fixed Group command (crash with GroupDeactivate and
    GroupClose,all)
-   (V31) Fixed "Control, ChooseString".
     Fincs provided the complete code for DllCall.  Thank you very much
    Fixed crash in internal function searchwindow.
     Fixed Run, /xxx/name.cab. Run was not able to start i.e. an
    document.
     Fixed WinWaitActive / Fixed ControlGet FindString / Fixed
    ControlGet Choice
     Fixed ReadRegString. Fincs reported a bug with a\_ComputerName.
    While reading the value from the registry the conversation between
    char and WCHAR was missed. This fix should solve a few other bugs,
    too / Fixed SendMessageTimeout. A lot of times the unsupported value
    SMTO\_ABORTIFHUNG was used. / Fixed SplitPath (crash)
-   (V32) (V62 SVN) Fixed RegWrite,REG\_MULTI\_SZ / Fixed Run / Fixed
    dllcall (unicode) / Fixed Control,ChooseString
-   (V33) Fixed GuiControlGet,\<blank\> / Fixed GuiControlGet,
    OutputVar, Focus / Fixed IniDelete when trying to delete a not
    existing key
-   (V34) Fixed A\_ThisMenuItemPos
-   (V35) Some didn't want tap-and-hold turned always on. I've added the
    directive \#DisableTapAndHold.
-   (V36) Fixed variables containing text of a giucontrol. If you enter
    an long text and then a short text, the string wasn't shorten.

Knows bugs / problems
---------------------

-   PixelGetColor and Click aren't working for 640x480. 1x1=2x2. Click,
    1,1 -\> = Click, 2,2 / Futurity: I used WinGetPos to get the windows
    position and size:
     Here are the results:
     Actual resolution of 800x480 is shown as 400x240 - FAIL
     Actual resolution of 640x480 is shown as 320x240 - FAIL
     Actual resolution of 400x240 is shown as 400x240 - PASS
-   Futurity: SendMessage FAIL PostMessage FAIL ControlSend FAIL
    ControlFocus FAIL
-   **emmanuel d:** A\_ThisMenuItemPos not working i am using it for
    dynamic menu's
-   WinWaitActive must be checked

Last change: 21-10-10

