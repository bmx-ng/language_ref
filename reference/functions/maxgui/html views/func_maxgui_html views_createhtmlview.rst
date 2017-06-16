.. _func_maxgui_html views_createhtmlview:

==============
CreateHTMLView
==============

CreateHTMLView - 

Description
===========

.. code-block:: blitzmax

    CreateHTMLView:TGadget(x,y,w,h,group:TGadget,style=0)

Create an HTMLView gadget.

The HTMLView is a complete web browser object inside a MaxGUI gadget. The HTML
page displayed is controlled with the #HTMLViewGo command or from the user navigating
from within the currently viewed page.

#CreateHTMLView supports the following styles:

[ @Style | @Meaning
* HTMLVIEW_NOCONTEXTMENU | The webpage's default context menu is disabled.
* HTMLVIEW_NONAVIGATE | User navigation is disabled and EVENT_GADGETACTION is generated instead.
]

[ @{Event ID} | @Description
* EVENT_GADGETDONE | Generated when a webpage has finished loading.
* EVENT_GADGETACTION | Generated when a user clicks a link. Event Text contains the requested URL.
]

%{Note: EVENT_GADGETACTION requires the HTMLVIEW_NONAVIGATE style flag.}

See Also: #HtmlViewGo, #HtmlViewBack, #HtmlViewForward, #HtmlViewStatus and #HtmlViewCurrentURL.

Parameters
==========

Return Values
=============

Nothing.

Examples
========

.. code-block:: blitzmax

    ' createhtmlview.bmx
    
    Import MaxGui.Drivers
    
    Strict 
    
    Local window:TGadget
    Local htmlview:TGadget
    
    window=CreateWindow("My Window",30,20,600,440,,15|WINDOW_ACCEPTFILES)
    
    htmlview=CreateHTMLView(0,0,ClientWidth(window),ClientHeight(window),window)
    SetGadgetLayout htmlview,1,1,1,1 
    
    HtmlViewGo htmlview,"www.blitzmax.com"
    
    While WaitEvent()
        Print CurrentEvent.ToString()
        Select EventID()
            Case EVENT_WINDOWCLOSE
                End
        End Select
    Wend

See Also
========



