.. figure:: ../_static/Images/trofmis3.png



***************************************************
Forest Canopy Density (FCD)
***************************************************
The FCD product in specified forests are generated using the Forest Canopy Density Model (FCD algorithm), as applied by (Rikimaru, et al, 2002). 
TroFMIS approach made slight modification to the original FCD technique, by excluding Principal Component Analysis (PCA),
which is computational intensive over large areas, or when computed using high resolution data. 
The modified FCD approach can be expressed as:

.. math::

 FCD=√(AVI × SSI+1)-1 
 :label: FCD model


Where, the Advanced Vegetation Index (AVI), like many vegetation index, gives precedence to the areas with healthier vegetation as
compraed to the areas with scarce or no vegetation. The AVI was computed as shown in the equation below.

.. math::

 AVI =  ((NIR+1)*(65536 -Red))*1/3
 :label: AVI model



The AVI was directly fused with Scaled Shadow Index (SSI), to yield the ultimate forest canopy densities.
i.e. areas with canopy cover while segregating areas with very little or no vegetation. 
SSI applied the numerical intergration of Blue and Green bands to identify shadow covered areas as shown in the equation below.

.. math::
 SSI=(256-Blue)*(256-Green)*(256-Red)/3
 :label: SSI model	
	
The figure below summarizes the steps of generating FCD product using earth observation based methods.

.. figure:: ../_static/Images/fcd_image.png
    :width: 300
    :align: center
    :height: 400
    :alt: service schema
    :figclass: align-center

    FCD computation summary.
    
 
Understanding Scripting of FCD
=============================================
FCD products were scripted using Javascript language in Google earth engine platform. The scripts computed the inidces and combined the
output to give the final FCD output.
In order to script the FCD outputs, it is vital that the following are defined.
* The Forest of Interest
* The specific year for product computation

Understanding the Basics of Satellite Imagery
==========================================================














FCD Data Encoding
=============================
The FCD product is rescaled to percentage, using a linear regression model.
The values are later reclassified into various Forest Canopy classes.
The percentage output values of this equation geovisualises areas of Dense Canopy, Moderate Canopy 
and Open Canopy between 100 to 65, 65 to 45, 45 to 30 respectively, while 
the Non- Forest areas were capped at below 30 percent as captured in the table below.

+------------------+-----------+---------+
| Sensor/Dataset   | Min       | Max     | 
+==================+===========+=========+
| Non Forest       | 0         | 30      | 
+------------------+-----------+---------+
| Open Canopy      | 30        | 45      | 
+------------------+-----------+---------+
| Moderate Canopy  | 45        | 65      | 
+------------------+-----------+---------+
| Dense Canopy     | 65        | 100     | 
+------------------+-----------+---------+


To compute the FCD output, the figure below summarises the steps applied in the computation.




.. figure:: ../_static/Images/fcd_flowchart.png
    :width: 350
    :align: center
    :height: 250
    :alt: service schema
    :figclass: align-center

    FCD computation summary.
    
    


  
.. figure:: ../_static/Images/trofmis3.png  
  


.. toctree::
   :maxdepth: 3



