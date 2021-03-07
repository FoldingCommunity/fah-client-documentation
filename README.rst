===========================================
Folding\@home Client Documentation - Readme
===========================================

To view near real-time formatting of the page as you edit, see https://foldinghome-client-documentation.readthedocs.io/en/latest/installation.html


Here's the badge to view Current Status of the documentation at readthedocs:

.. image:: https://readthedocs.org/projects/foldinghome-client-documentation/badge/?version=latest
   :target: https://foldinghome-client-documentation.readthedocs.io/en/latest/?badge=latest
   :alt: Documentation Status

Alternatively, read the documentation online at http://foldinghome-client-documentation.rtfd.io/


Quick Tutorial/Tips
===================

--------
Headings
--------

Heading formatting/styling is actually free by your style. You just need to be consistent within a single document.

I recommend using this format::

   ==========
   Page Title
   ==========

   Section 1
   =========

   ----------------------
   Subsection 1 (Level 2)
   ----------------------

   Sub-subsection (Level 3)
   ------------------------

You can also use ``" .`` as other option. For more you can try look for it, I believe there's more characters that can be used.


------------
Text Styling
------------

Some basic styling::

   **Bold**
   *Italic*
   ``monospaced``

   ------------------------

   Escape certain special characters using "Backslash", example: Folding\@Home
   It is because rst will automatically parse to action link "mailto" when see "@" character. 
   Except if @ is inside a styling, e.g. **Folding@Home** doesn’t need to be **Folding\@Home**.

      a Tab
   
   | Line 1
   | Change Line (Line 2 with no space between Line)

   ----------------------------------------------------------------------

   Adding footnote [1]_ also this one too [2]_

   .. [1] `Hopkins, 2002 <http://www.ncbi.nlm.nih.gov/pubmed/12209152>`_
   .. [2] `Bowman, 2012 <http://www.pnas.org/content/109/29/11681>`_

   ----------------------------------------------------------------------

   .. role:: strike

   :strike:`This text is crossed out`

   ----------------------------------------------------------------------

   .. rst-class:: center

   This paragraph will be centered.

   ----------------------------------------------------------------------


-----
Links
-----

Example::

   `Foldingforum.org <https://foldingforum.org/>`_
   `Discord <http://discord.gg/foldingathome>`_

   Note: if you define the same target name in the same page, you need to use double underscore at the end instead to avoid warning.


------
Images
------

Example::

   .. image:: directory/image1.png

   to add image that being placed in specific directory from where your working page is.

   .. image:: https://foldingathome.org/wp-content/uploads/2016/09/Pande-Lab_Stanford-University_Foldingathome-2.jpg
      :alt: FAQ
      :align: center
      :height: 100
      :width: 200

   to add image from a link and also optionally you can add styling.


-----------------------
Local Table of Contents
-----------------------

Use this formatting to create a local page table of contents. This formatting must be added directly to the identified .rst doc.::

   .. contents::
      :local:


-----
Lists
-----

Use this formatting to create an indented bulleted list::

   - list 1
   - list 2
   - list 3

Use this formatting to create a numbered list::

   1. List (1)
   2. List (2)
   3. List (3)
   #. For auto-enumerated (4)


----------------
Additional Notes
----------------
| If you're checking the docs, you will need several minutes for readthedocs to build the documentation first.
| A good reStructuredText reference: https://docutils.sourceforge.io/docs/user/rst/quickref.html

.. This is a comment
   Special notes that are not shown but might come out as HTML comments
   .. contents:: Table of Contents
   :depth: 2
   contact link
   faq link
   rulesnpolicies link
   miscellaneous image
   windows_custom_installation image 14
   configuration_installation image 7
   