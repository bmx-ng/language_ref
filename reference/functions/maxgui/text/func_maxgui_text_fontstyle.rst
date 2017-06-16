.. _func_maxgui_text_fontstyle:

=========
FontStyle
=========

FontStyle - 

Description
===========

.. code-block:: blitzmax

    FontStyle(font:TGuiFont)

Retrieves the corresponding property from the TGuiFont type instance.
The returned value will be a combination of the following flags:

[ @Constant | @{Font Style}
* FONT_BOLD | Bold
* FONT_ITALIC | Italic
* FONT_UNDERLINE | Underlined
* FONT_STRIKETHROUGH | *StrikeThrough
]

%{Note: FONT_STRIKETHROUGH isn't fully supported by all gadgets/platforms.}

See Also: #LoadGuiFont, #RequestFont, #FontName and #FontSize

Parameters
==========

Return Values
=============

An integer representing the style of the font (e.g. Bold, Underlined, Italics).

Examples
========

See Also
========



