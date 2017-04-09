BASICODE interpreter
====================

This is a BASICODE interpreter in Javascript, compatible with BASICODE versions 2, 3 and 3C. It's free & open source, released under the Expat MIT licence.
There is `a live demo <http://robhagemans.github.io/basicode/>`_.

`BASICODE programs <https://github.com/robhagemans/basicode>`_ are available in a separate repository.


Quick start
-----------
::

    <!DOCTYPE html>
    <html>
    <head>
        <script src="basicode.js"></script>
    </head>
    <body>
        <script type="text/basicode">
            1010 PRINT "Hello, world!"
        </script>
    </body>
    </html>


Deployment
----------

The package consists of a single Javascript file. To embed one or more interpreters in an HTML5 document, link the script in the header.
It will scan the HTML for any ``<script type="text/basicode">`` elements and replace them with newly created canvases.

- If the element contains any content or has a ``src=`` property pointing to a text file, the script will attempt to execute it as BASICODE.
- If the element is empty, it will show a splash screen.

In either case, you can drag and drop local text files containing BASICODE onto the canvas to execute them. Enjoy!


Settings
--------

A number of options can be set through the dataset attribute of the ``script`` element:

===================== =======================================================================
Attribute             Setting
===================== =======================================================================
``data-columns``      Number of text columns
``data-rows``         Number of text rows
``data-speed``        Number of cycles per second in ``FOR`` loops (roughly)
``data-font``         Font to use for text. See below.
``data-color-0``      Set the value for colour 0 (background)
``data-color-7``      Set the value for colour 7 (foreground). Other colours can be set too.
``data-canvas``       Target ``canvas`` id for screen / keyboard
``data-floppy``       Target ``div`` id for visualisation of floppy drive
``data-printer``      Target ``iframe`` id for printer output
``data-load``         Name of global Javascript function to call on loading a new program
===================== =======================================================================


Fonts
-----

The following fonts are available:

============== ===== ======================================
Font           Size  Description
============== ===== ======================================
``smooth``           Browser's native monospace font
``tiny``       6x4   A very small bitmap font
``apple``      7x8   Apple-II font
``msx``        7x8   MSX font
``atari``      8x8   Atari 8-bit font
``bbc``        8x8   Acorn BBC Micro font
``c64``        8x8   Commodore 64 font
``cpc``        8x8   Amstrad/Schneider CPC font
``exidy``      8x8   Exidy Sorcerer font
``genie1``     8x8   EACA Colour Genie 1st font
``genie2``     8x8   EACA Colour Genie 2nd font
``kc85``       8x8   Robotron KC85/1 font
``pcw``        8x8   Amstrad PCW/Schneider JOYCE font
``spectrum``   8x8   Sinclair ZX Spectrum font
``vic``        8x8   Commodore PET and VIC-20 font
``cga``        8x8   IBM CGA font
``thin``       8x8   IBM CGA thin stroke font
``pcjr``       8x8   IBM PCjr font
``tandy``      8x8   Tandy 1000 font
``tandy2``     8x8   Tandy 1000 font, later version
``p2000``      8x10  Philips P2000T font
``coco``       8x12  Tandy TRS-80 CoCo v1&2 font
``coco3``      8x12  Tandy TRS-80 CoCo v3 font
``mpf``        8x12  Multitech Micro-Professor MPF-I font
``ega``        8x14  IBM EGA font
``mda``        9x14  Hercules and IBM MDPA font
``olivetti``   8x16  Olivetti M24 and AT&T 6300 font
``vga``        9x16  IBM VGA font
``wyse-serif`` 16x16 Wyse WY-700 serif font
``wyse-sans``  16x16 Wyse WY-700 sans serif font
============== ===== ======================================


Compatibility
-------------

The interpreter should work on reasonably recent, standards-compliant browsers.
You need a keyboard, so it will be difficult to use on mobile.
I've superficially tested it on Chrome, Firefox, Safari, and Opera.
It probably works fine on Edge, but I haven't tried. It mostly works on Internet Explorer 11 (except sound) but not at all on older versions.
