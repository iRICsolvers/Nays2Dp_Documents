Introduction
============

Nays2d+ is a quasi 3-dimensional open channel flow solver, which combines the results of horizontal 2-dimensional 
shallow water flow model and a theoretical solution of velocity profiles of main flow and secondary 
flow profiles in vertical direction.  The results of the flow solution of Nays2dh in iRIC are 
used for basic 2-dimensional flow field, and the theory proposed by Engelund(1974) :math:`^{1)}` is superimposed
over the 2-dimensional solution.
Followings are main procedure of the calculation of Nays2d+.

- Calculate the depth averaged flow field in a general coordinate sysytem by Nays2dh.
- Calculate the streamline of the depth averaged velocity.
- Calculate the radius of curvature of the streamline.
- Calculate the main flow an secondary flow profile using the stream line curvature, water depth and depth averaged velocity 
- Put these velocity profiles back to the general coordinate system
- Show the results in the iRIC GUI windows

In general, fully non-hydrostatic 3-dimensional models are more accurate for the detailed flow analyses, however, they are usually much more time consuming than 2-dimensional models, and have some difficultie in calculating free water surface.  
On the other hand, the computational time of the Nays2d+ is much less because it is based on a hydrostatic 2-dimensional model, and three dimensional components are superimposed using a theoretical solution of fully developed secondary flow in curved channels.  Of cause non-hydrostatic 3-dimensional models are required when the flow is very complicated and the magnitude of the vertical acceleration is much larger than acceleration due
to gravity.  But in the most of the cases we deal with, hydrostatic assumption are good enough especially in natural rivers.   
In Nays2d+, the computational time is much less than fully non-hydrostatic 3-dimensional models as `Nays3dv <https://i-ric.org/yasu/Nays3dv/index.html>`_ and much more stable even when the depth becomes very shallow or zero.
The secondary flow theory used in Nays2d+ is by 
`Engelund(1974) <https://cedb.asce.org/CEDBsearch/record.jsp?dockey=0022331>`_ .
The equations used in Nays2d+ to construct quasi 3-dimensional flow field are summarized 
`here <https://i-ric.org/yasu/refs/SecondaryFlowEqs_EN.pdf>`_ .
Nays2d+ can be operational in `iRIC <https://i-ric.org/>`_ version 3.x or later.

.. figure:: images/Ishikari.gif


.. figure:: images/yasu.png
   :width: 50%
   :target: https://rivmodel.rivpac.com/

.. figure:: images/iric.jpg
   :width: 50%
   :target: https://i-ric.org/

22 Fbrually 2021
`Yasu Shimizu <https://rivmodel.rivpac.com/>`_

