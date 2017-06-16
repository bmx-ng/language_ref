.. _func_maxgui_text areas_formattextareatext:

==================
FormatTextAreaText
==================

FormatTextAreaText - 

Description
===========

.. code-block:: blitzmax

    FormatTextAreaText( textarea:TGadget,r,g,b,flags,pos=0,length=TEXTAREA_ALL,units=TEXTAREA_CHARS )

Format the color and style of some text in a TextArea gadget.

The @r, @g and @b parameters represent the @{r}ed, @{g}reen and @{b}lue components (0..255)
which, when combined, represent the new text color for the the sepecified region
of characters.

The @flags parameter can be a combination of the following values:

[ @Constant | @Meaning
* TEXTFORMAT_BOLD | Bold
* TEXTFORMAT_ITALIC | Italic
* TEXTFORMAT_UNDERLINE | Underline
* TEXTFORMAT_STRIKETHROUGH | StrikeThrough
]

Depending on the value of the units parameter the position and length parameters specify
the character position and number of characters or the starting line and the number
of lines that FormatTextAreaText will modify.

See Also: #LockTextArea and #CreateTextArea

Parameters
==========

Return Values
=============

Nothing.

Examples
========

See Also
========



