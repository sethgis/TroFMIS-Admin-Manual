.. figure:: ../_static/Images/trofmis3.png

.. note::
   This is note text. Use a note for information you want the user to
   pay particular attention to.

   If note text runs over a line, make sure the lines wrap and are indented to
   the same level as the note tag. If formatting is incorrect, part of the note
   might not render in the HTML output.

   Notes can have more than one paragraph. Successive paragraphs must
   indent to the same level as the rest of the note.

.. warning::
    This is warning text. Use a warning for information the user must
    understand to avoid negative consequences.

    Warnings are formatted in the same way as notes. In the same way,
    lines must be broken and indented under the warning tag.













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



