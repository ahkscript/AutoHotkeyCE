# TODO

<http://www.autohotkey.com/forum/viewtopic.php?p=342593\#342593>

However, if you try it again a second time, typing a shorter string
into the box (e.g. "XYZ"), the "After" message box will appear with
"XYZ123456" in it... of course it should just be "XYZ".

* * * * *

http://www.autohotkey.com/forum/viewtopic.php?p=328862\#328862
just found another problem I would be happy if someone knows a solution
for:

I want to replace the existing text/label of (alltogether) text controls.

So within a loop I normally would do

   GuiControl,, MyTextControl, NewText or
   GuiControl,Text , MyTextControl, NewText

However on my device this leads to the new text written above the old
one.

What seems to miss is a kind of redrawing of the control:
If I hide the controls and show them again, the old text has vanished.
However this isn't really a solution as it makes the whole process very
slow...

So when looping over only 8 controls, it takes 1-2 seconds to refresh
the contents. Unfortunately I need them to be rather responsive as
they"re updated quite often (kinf of context buttons).

Another question - probably rather advonced - how do I get rid of the
tap and hold gesture? Sorry, I'm aware it was sure difficult to
implement, but in my case it's rather annoying (I'm trying kind of mouse
gestures).


* * * * *

<http://www.autohotkey.com/forum/viewtopic.php?p=311233\#311233>

Here is my script for importing certificates. There are two CA's and
one user's with private key. Sometimes it runs properly and sometimes
hangs on WinWaitActive (the WinActivate was not enough)... What is kind
of strange - the script usually hangs on WinWaitActive,Import?
  
   Send {LWin}
   Sleep,1000
   Send s
   Sleep,1000
   Send c
   Sleep,1000
   Send c
   Sleep,1000
   Send {Enter}
   
   WinActivate,Certificates
   WinWaitActive,Certificates
   Send !i
   WinActivate,Import


It looks like there is really something wrong with WinWaitActive.
I think the line

   048: WinWaitActive,Root,1 (159.99)

 should never be reported in the script log...

* * * * *

28-03-10

<http://www.autohotkey.com/forum/viewtopic.php?p=298776\#298776>

A\_ThisMenuItemPos not working. I am using it for dynamic menu's
 is this on the list to add .i'm doing something like this:

   menutest() {
   CoordMode, Menu, Screen
     Menu, test, add, Test1, MenuHandler
     Menu, test, add, Test2, MenuHandler
     Menu, test, add, Test3, MenuHandler
     Menu, test, add, Test4, MenuHandler
     Menu, test, add, Test5, MenuHandler
     Menu, test, Show, 0, 380
     return
     }
  
   MenuHandler:
     {
     msgbox,% "A\_ThisMenu:" A\_ThisMenu " \`nA\_ThisMenuItemPos:" A\_ThisMenuItemPos "\`n "%A\_ThisMenu%%A\_ThisMenuItemPos%Link
     return
     }

* * * * *

19-12-09 Debugged a few days a phantom error. If you are using an
emulator and pressing i.e. '\<' on the Windows keyboard the hotkey is
not fired. If you're using the virtual keyboard of the emulator, the
hotkey is working. Perhaps it's just an localization problem, because
I'm using a german keyboard and the virtual keyboard of the emulator is
an english one. Needs further investigation.

* * * * *

04-04-10 The compiler should use the provided icon file and not
hardcoded the ahk-icon

Wishes from the community:  
support "sdi"? windows


Last change: 19-12-09