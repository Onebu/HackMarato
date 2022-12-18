# HackMarato

## Preprocessing




## Measurements

The measurements are done in the notebook final_pipeline.ipynb.

The user needs to manually interpret the heart rate (HR) and the minimum and maximum values on the scale. These values should be typed into the notebook at the allocated space (HR, min_scale_SAX, max_scale_SAX, min_scale_PSLA, max_scale_PSLA).

The program measures the SAX images first, and afterwards the PSLA images. At the end, it calculates the average obtained values for the parameters. 
OBS: The lists of parameter values do not empty before each run unless you run the cell in the beginning where the empty lists are created. This means that to obtain the correct values, the user must run the SAX cell directly followed by the PSLA cell and then immediately calculate the average values. Otherwise the list of parameter values will contain duplicated measurements. 

At the end of the notebook, the output indicates whether or not the heart is sick. 