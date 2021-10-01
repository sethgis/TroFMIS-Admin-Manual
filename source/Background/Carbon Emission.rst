.. figure:: ../_static/Images/trofmis3.png



***************************************************
Forest Carbon Flux (Carbon Emission)
***************************************************
Carbon flux product is generated from the Reference product computed from the difference between the comparison period (2016) and consequent years (2017, 2018, 2019, 2020).

The referenced products are first classified into two classes (Forest and Non Forest areas).
The classified products are then used to compute the difference between the analysis period and the comparison period.
The assumption made, is that the forest monitored is an instant forest, and any change in class depicts either carbon emitted or carbon enhanced.

The resultant Carbon flux product, provides information on estimated carbon transferred from the above ground pool to the atmosphere, or the vice versa (sequestration) when afforestation/reforestation or regrowth occurs.
To estimate the carbon stocks, the above ground biomass (AGB) stocks in the Tropical Forests of the Eastern Africa region, are estimated based on the 2006 IPCC guidelines.
For Tropical rain forests, the AGB is estimated at 310 Mg Biomass/ha, which is converted to 145.7 Mg Carbon/ha and translated to 534 Mg CO2 eq/ha 
(CO2 is carbon dioxide). 
Based on the above emission factors, and the deforested forest areas (Activity Data), between two time intervals, Emission estimates (E) is estimated as shown in the formula below.

.. math::
 E = AD*EF	 
 :label: Carbon Emission Equation

With AD being the change of forest cover in hectares (Deforestation - AD) and the reference value of 
carbon stock density per hectare in tropical forests (EF – Reference Value (Integer)).

The carbon flux was computed from the binary class of forest and non-forest class, where the difference between the Analysis period, and the reference year 2016 was generated, as is shown in the table below.

+------------------+-----------+---------+---------------+
| Sensor/Dataset   | Min       | Max     |               |  
+==================+===========+=========+===============+
| Non Forest       | 0         | 30      |  Non Forest   |  
+------------------+-----------+---------+---------------+
| Open Canopy      | 30        | 45      |               |  
+------------------+-----------+---------+   Forest      +
| Moderate Canopy  | 45        | 65      |               |  
+------------------+-----------+---------+               +
| Dense Canopy     | 65        | 100     |               |  
+------------------+-----------+---------+---------------+

To compute the carbon flux, please consider the steps as illsutrated below.

* Surpose you get the pixel count as above, go ahead and calculate the net changes

+------------------+-----------+
| Class            |Pixel Count|  
+==================+===========+
| Stable           | 11143909  | 
+------------------+-----------+
| Loss             |391764     |
+------------------+-----------+
| Gain             | 173370    |
+------------------+-----------+



 .. code-block:: bash
							
		Compute the net change.							

		Net Changes	Gain - Loss

		(173370 subtract 391764)

		Net Change	173370					

		After Getting the net change, some conditions have to be met							

		   * If the change is positive (+), then there was carbon enhancement						
		   * If the change is negative (-), then there is carbon loss						
		   * Get the carbon flux (emmission) by first transforming the Net Change to hectares, and then multiply by 145.7 Mg C/ha							

		Net Change (Ha)	1722.7					

		   - Carbon Emmission	250997.39	Mg C/ha	per year	

		The figure below summarises the steps of computing the carbon flux in TroFMIS.

The carbon flux statistics are generated as shown in the illustrated steps above, different from the other products which are based on pixel counts in hectares.
Please refer to the code as is shown below.

.. figure:: ../_static/Images/ref_product.png
    :width: 500
    :align: center
    :height: 400
    :alt: service schema
    :figclass: align-center
    
    
    
.. figure:: ../_static/Images/trofmis3.png  
    
.. toctree::
   :maxdepth: 3
   
