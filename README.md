# HackMarato

## Preprocessing

The preprocess procedures are done in the notebook preprocess.ipynb.

The users has to select one of the videos first to cut the videos into frames and retrieve the Motion mode from each images, and we also store the maximum and minimum scales from this mode to get the reference point for the measurement.

The process function receives 5 parameters:
- path: the source images of cutted motion mode we want to process
- thresh_medium: the threshoding parameter for the medium parts results, recomended value: 25.
- thresh_higher:the threshoding parameter for the higher parts results, recomended value: 15.
- thresh_lower: the threshoding parameter for the lower parts results, recomended value: 60.
- h: the height of the rectangle to block the top parts of the images to improve the results of higher and lower part.


## Measurements

The measurements are done in the notebook final_pipeline.ipynb.

The user needs to manually interpret the heart rate (HR) and the minimum and maximum values on the scale. These values should be typed into the notebook at the allocated space (HR, min_scale_SAX, max_scale_SAX, min_scale_PSLA, max_scale_PSLA).

The program measures the SAX images first, and afterwards the PSLA images. At the end, it calculates the average obtained values for the parameters. 
OBS: The lists of parameter values do not empty before each run unless you run the cell in the beginning where the empty lists are created. This means that to obtain the correct values, the user must run the SAX cell directly followed by the PSLA cell and then immediately calculate the average values. Otherwise the list of parameter values will contain duplicated measurements. 

At the end of the notebook, the output indicates whether or not the heart is sick. 