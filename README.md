# Polarization
Polarization.py is a Python module for generating a surface normal map given polarization images from 0, 45, 90 and 135 degree filters. These images are obtained from a single image displaying the four images from the different filters in quadrants. The instrument used was the FLIR Blackfly S Machine Vision camera. In order to calculate the surface normals, intermediate processes are done such as calculating angle and degree of linear polarization images, building an object mask, calculating ambiguous surface normals at four orientations, finding the coordinates for the line of ambiguity, building masks for hemispheres separated by the line of ambiguity and finally producing a fully disambiguated surface normal map. For more information on these intermediate steps, visit https://wiki.compacsort.com/display/EPP/DIS999998+Structure+from+Polarisation+project.

## Dependencies
The following modules are needed by Polarization.py.

-numpy\
-cv2\
-cmath\
-scipy.signal\
-PIL\
-matplotlib.pyplot\

These will be imported as follows:

```python
import numpy as np
import cv2
import cmath
from scipy.signal import savgol_filter
from PIL import Image
import matplotlib.pyplot as plt
```
## Usage
In order to run Polarization.py on a polarization image, change the global FILENAME variable assigned at the start to the address of your chosen file. 

```python
FILENAME = 'C:\\Users\\akharbanda\\.spyder-py3\\Asymmetrical Fruit\\quad3.tiff'
```
 
    
