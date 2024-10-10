# neuromorphic-event-based-camera-code

space for collecting findings and information regarding event based cameras and their use in FSOC
# event based camera
typically data is packeaged into a format e_k = [x_k,y_k,t_k,p_k]
x,y coordinate, time, polarity(rising edge or falling edge)
_____


# FSOC
https://ieeexplore.ieee.org/document/1577553 
FSOC wavelength windows - 825nm 1330nm 1550nm 

typical free space loss is 20 dB (for a point to point system)  -- if we can still detect/communicate with a lower loss than we do better than a typical point to point.

Atmospheric loss
This may cause polarization fluctuations, beam steering, image dancing, beam spreading and scintillation. Scintillation causes the amplitude of the received signal to fluctuate rapidly by as much as 30 dB with power spectral density spanning 0.01–200 Hz, and hence give rise to long bursts of data errors.
_____
optical characterisation of the atmosphere
https://ntrs.nasa.gov/api/citations/20190001012/downloads/20190001012.pdf

Considering low earth orbit satellites and optical ground station links
https://onlinelibrary.wiley.com/doi/10.1002/sat.1426
using the water vapor, co2 absorption and other aerosol absorption spectra, a region of wavelengths best suited for this is between 1550nm. close to the optical CLU bands. 
(might be useful to follow the maths and show what is best within the 0 - 10km atmosphere region.) (airplanes fly about 8 - 11km)

_____


