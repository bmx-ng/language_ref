.. _func_maxgui_menus_createmenu:

==========
CreateMenu
==========

CreateMenu - 

Description
===========

.. code-block:: blitzmax

    CreateMenu:TGadget( text$,tag,parent:TGadget,hotKey=0,modifier=0 )

Create a menu.
Menu gadgets should be attached to either a #WindowMenu, other Menu gadgets
or used with the #PopupWindowMenu command. The tag field should be a unique identifier
that will be present in the #EventData field of EVENT_MENUACTION events.

Keyboard shortcuts can be associated with a Menu by using the optional hotKey and
modifier parameters.

Please refer to the #{key codes} module for valid key and modifier codes.
The MODIFIER_COMMAND value should be used instead of MODIFIER_CONTROL
with Menu hotkeys for best crossplatform compatability.

Menus now also support icons on most platforms through the use of #SetGadgetPixmap.

See Also: #FreeMenu, #SetMenuText, #CheckMenu, #UncheckMenu, #EnableMenu, #DisableMenu,
#MenuText, #MenuChecked, #MenuEnabled and #SetGadgetPixmap.

Parameters
==========

Return Values
=============

Nothing.

Examples
========

.. code-block:: blitzmax

    ' createmenu.bmx
    
    Import MaxGui.Drivers
    
    Strict 
    
    Local window:TGadget
    Local filemenu:TGadget
    Local editmenu:TGadget
    Local helpmenu:TGadget
    
    Const MENU_NEW=101
    Const MENU_OPEN=102
    Const MENU_SAVE=103
    Const MENU_CLOSE=104
    Const MENU_EXIT=105
    
    Const MENU_CUT=106
    Const MENU_COPY=107
    Const MENU_PASTE=108
    
    Const MENU_ABOUT=109
    
    window=CreateWindow("My Window",40,40,320,240)
    
    filemenu=CreateMenu("&File",0,WindowMenu(window))
    CreateMenu"&New",MENU_NEW,filemenu,KEY_N,MODIFIER_COMMAND
    CreateMenu"&Open",MENU_OPEN,filemenu,KEY_O,MODIFIER_COMMAND
    CreateMenu"&Close",MENU_CLOSE,filemenu,KEY_W,MODIFIER_COMMAND
    CreateMenu"",0,filemenu
    CreateMenu"&Save",MENU_SAVE,filemenu,KEY_S,MODIFIER_COMMAND
    CreateMenu"",0,filemenu
    CreateMenu"E&xit",MENU_EXIT,filemenu,KEY_F4,MODIFIER_COMMAND
    
    editmenu=CreateMenu("&Edit",0,WindowMenu(window))
    CreateMenu "Cu&t",MENU_CUT,editmenu,KEY_X,MODIFIER_COMMAND
    CreateMenu "&Copy",MENU_COPY,editmenu,KEY_C,MODIFIER_COMMAND
    CreateMenu "&Paste",MENU_PASTE,editmenu,KEY_V,MODIFIER_COMMAND
    
    helpmenu=CreateMenu("&Help",0,WindowMenu(window))
    CreateMenu "&About",MENU_ABOUT,helpmenu
    
    UpdateWindowMenu window
    
    While True
        WaitEvent 
        Select EventID()
            Case EVENT_WINDOWCLOSE
                End
            Case EVENT_MENUACTION
                Select EventData()
                    Case MENU_EXIT
                        End
                    Case MENU_ABOUT
                        Notify "Incrediabler~n(C)2005 Incredible Software"
                End Select
        End Select
    Wend

See Also
========



