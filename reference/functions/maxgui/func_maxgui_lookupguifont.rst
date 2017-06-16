.. _func_maxgui_lookupguifont:

=============
LookupGuiFont
=============

LookupGuiFont - 

Description
===========

.. code-block:: blitzmax

    LookupGuiFont:TGuiFont( pFontType% = GUIFONT_SYSTEM, pFontSize:Double = 0, pFontStyle% = 0 )

Returns a suitable GUI font that best matches the type of font specified.
If the current MaxGUI driver doesn't return a suitable GUI font, then
a hard-coded fall-back font is returned instead, depending upon the platform:

@pFontType can take one of the following constants:

[ @Constant | @{Windows Fall-Back} | @{Mac OS X Fall-Back} | @{Linux Fall-Back} | @Description
* GUIFONT_SYSTEM | MS Shell Dlg | Lucida Grande | FreeSerif | Default font used to draw gadgets by the OS.
* GUIFONT_SERIF | Times New Roman | Times New Roman | FreeSerif | Serif font.
* GUIFONT_SANSSERIF | Arial | Helvetica | FreeSans | Sans Serif font.
* GUIFONT_SCRIPT | Comic Sans MS | Comic Sans MS | TSCu_Comic | Handwriting style font.
* GUIFONT_MONOSPACED | Consolas/Courier New | Courier | Courier | Fixed width font typically used for coding.
]

@pFontSize specifies the font size the font should be loaded with. If this value is less than or equal to 0, then
the current MaxGUI driver chooses a suitable size, or a hard-coded alternative is used (usually 10/11/12pt).

@pFontStyle specifies any addition font styles the font should be loaded with. A combination of any of the
following flags can be used:

[ @Constant | @{Font Style}
* FONT_BOLD | Bold
* FONT_ITALIC | Italic
* FONT_UNDERLINE | Underlined
* FONT_STRIKETHROUGH | StrikeThrough
]

%{Note: FONT_STRIKETHROUGH isn't fully supported by all gadgets/platforms.}

See Also: #RequestFont, #FontName, #FontSize and #FontStyle

Parameters
==========

Return Values
=============

A suitable new @TGuiFont instance matched with the parameters supplied.

Examples
========

.. code-block:: blitzmax

    ' lookupguifont.bmx
    
    Strict
    
    Import MaxGUI.Drivers
    
    AppTitle = "LookupGuiFont() Example"
    
    Const strSampleText$ = "Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Nulla eget mauris quis dolor "+..
    "ullamcorper dapibus. Duis facilisis ullamcorper metus. Pellentesque eget enim. Vivamus auctor hendrerit turpis. " + ..
    "Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia Curae
     Vivamus tincidunt leo quis urna." 
    
    Const intWindowFlags% = WINDOW_TITLEBAR|WINDOW_RESIZABLE|WINDOW_STATUS|WINDOW_CLIENTCOORDS
    
    Global wndMain:TGadget = CreateWindow( AppTitle, 100, 100, 500, 300, Null, intWindowFlags )
        SetMinWindowSize( wndMain, ClientWidth(wndMain), ClientHeight(wndMain) )
    Global lstFontTypes:TGadget = CreateListBox(0,0,200,ClientHeight(wndMain),wndMain)
        SetGadgetLayout lstFontTypes,EDGE_ALIGNED,EDGE_CENTERED,EDGE_ALIGNED,EDGE_ALIGNED
        AddGadgetItem lstFontTypes, "GUIFONT_SYSTEM", GADGETITEM_DEFAULT, -1, "Default OS font.", LookupGuiFont(GUIFONT_SYSTEM)
        AddGadgetItem lstFontTypes, "GUIFONT_SERIF", 0, -1, "Serif font.", LookupGuiFont(GUIFONT_SERIF)
        AddGadgetItem lstFontTypes, "GUIFONT_SANSSERIF", 0, -1, "Sans serif font.", LookupGuiFont(GUIFONT_SANSSERIF)
        AddGadgetItem lstFontTypes, "GUIFONT_SCRIPT", 0, -1, "Script/handwriting font.", LookupGuiFont(GUIFONT_SCRIPT)
        AddGadgetItem lstFontTypes, "GUIFONT_MONOSPACED", 0, -1, "Fixed width/coding font.", LookupGuiFont(GUIFONT_MONOSPACED)
    
    Global txtPreview:TGadget = CreateTextArea(200,0,300,ClientHeight(wndMain),wndMain,TEXTAREA_WORDWRAP|TEXTAREA_READONLY)
        SetGadgetLayout txtPreview,EDGE_ALIGNED,EDGE_ALIGNED,EDGE_ALIGNED,EDGE_ALIGNED
        SetTextAreaText( txtPreview, strSampleText )
    
    Global strFontString$
    
    ChooseFont( LookupGuiFont() )
    
    Repeat
        Select WaitEvent()
            Case EVENT_APPTERMINATE, EVENT_WINDOWCLOSE
    End
            Case EVENT_GADGETACTION, EVENT_GADGETSELECT
                Select EventSource()
                    Case lstFontTypes
                        If EventData() >= 0 Then
                            ChooseFont( TGuiFont(GadgetItemExtra( lstFontTypes, EventData() )) )
                        EndIf
                EndSelect
        EndSelect
        SetStatusText( wndMain, strFontString + "~t~t" + CurrentEvent.ToString() + "   " )
    Forever
    
    Function ChooseFont( pFont:TGuiFont )
        SetGadgetFont( txtPreview, pFont )
        strFontString$ = FontName(pFont) + ", " + Int(FontSize(pFont)) + "pt"
    EndFunction

See Also
========



