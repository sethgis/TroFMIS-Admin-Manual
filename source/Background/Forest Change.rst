
.. figure:: ../_static/Images/trofmis3.png


***************************************************
Forest Canopy Change (FCC)
***************************************************
FCC product maps the drop or regrowth in canopy densities that have occured within a period, either as a difference from the 
consequent years or a difference from a comparison (baseline) period i.e 2016.
The computation of the difference highlights areas that have since experienced canopy disturbance, regrowth or are stable. 
The computation is based on a simple image difference between the comparison period and analysis period.
To compute FCC, two approaches are majorly employed, including.

       * Changes based on the Reference year i.e 2016 (Reference Product).
       * Changes based on the difference between the consequent year (Annual Product).

Reference Product
============================
Reference Products are achieved after computing the difference between the compasrison year\baseline year (2016),
and the other consequent years i.e 2017, 2018, 2019 & 2020. This product detects the deforestation that occurs in comparison
to the baseline year which is 2016. The output and statistics assumes the forest zones are instant forest.
Classifying the forest canopy densities, makes it possible to monitor forest disturbances every year, in each forest of interest.

Annual Product
============================
The changes are computed in comparison to the consequent years. In monitoring the forest regrowth between two years, this product can be applied.
The changes are generated after computing the difference between the forest canopy densities from 2016 - 2020
The products available are in the TroFMIS 2016 - 2017, 2017 - 2018, 2018 - 2019 & 2019 - 2020, and the updating of newer products will be done once the satellite images for the entire year are available.

The figure below shows the summary of computing the forest changes.

.. figure:: ../_static/Images/Canopy_Disturbance.png
    :width: 351
    :align: center
    :height: 341
    :alt: service schema
    :figclass: align-center

    Forest Canopy Changes computation.
   
Computing the FCC products in Google Earth Engine
======================================================== 
The code provided in the Forest Canopy Density section, provides a multi products as outputs, and this include both the 
* Forest Canopy Densities and
* Forest Canopy Changes both annual and Reference product. 

The description of the screen shot below from the main code highlights how the Changes are generated.

.. figure:: ../_static/Images/ref_product.png
    :width: 351
    :align: center
    :height: 341
    :alt: service schema
    :figclass: align-center


 
 
.. figure:: ../_static/Images/trofmis3.png

.. toctree::
   :maxdepth: 3
