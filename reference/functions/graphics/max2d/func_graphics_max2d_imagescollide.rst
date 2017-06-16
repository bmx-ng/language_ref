.. _func_graphics_max2d_imagescollide:

=============
ImagesCollide
=============

ImagesCollide - 

Description
===========

.. code-block:: blitzmax

    ImagesCollide(image1:TImage,x1,y1,frame1,image2:TImage,x2,y2,frame2)

Tests if two images collide

#ImagesCollide uses the current Rotation and Scale factors from the most previous
call to #SetScale and #SetRotation to calculate at a pixel level if the two images collide.

Parameters
==========

Return Values
=============

True if any pixels of the two images specified at the given location overlap.

Examples
========

See Also
========



