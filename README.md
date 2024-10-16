# neuromorphic-event-based-camera-code

space for collecting findings and information regarding event based cameras and their use in FSOC
# event based camera
typically data is packeaged into a format e_k = [x_k,y_k,t_k,p_k]
x,y coordinate, time, polarity(rising edge or falling edge)

sony/prophesee img646 sensor
https://ieeexplore.ieee.org/abstract/document/9063149

https://ieeexplore.ieee.org/document/8495003
(improved cooling means better contrast detection so investigating temperature operating conditions and when it is the best is an option)
paper also argues that an event based camera performs poorly in low light conditions, this could be an effect up for investigation, whether it actually performs poorly in low light.

https://ieeexplore.ieee.org/document/9852890
cubesat launched tracker 

A. Strengths
High Temporal Resolution: Monitoring of brightness changes is fast in analog circuitry, and the read-out of the events is digital, with a 1 MHz clock, i.e., events are detected and timestamped with microsecond resolution. Therefore, event cameras can capture very fast motions, without suffering from motion blur typical of traditional cameras.

Low Latency: Each pixel works independently and there is no need to wait for a global exposure time of the frame. As soon as the change is detected, an event is transmitted. Hence, event cameras have minimal latency: about 10 μs on the lab bench, and sub-millisecond in the real world.

High Dynamic Range (HDR): The very high dynamic range of event cameras (>120 dB) notably exceeds the 60 dB of high-quality, frame-based cameras, making them able to acquire information from moonlight to daylight. It is due to the facts that the photoreceptors of the pixels operate in logarithmic scale and each pixel works independently, not waiting for a global shutter. Like biological retinas, DVS pixels can adapt to very dark as well as very bright stimuli.

Low Bandwidth: Event cameras transmit only brightness changes and thus remove redundant data. For SSA, most pixels reflect the universe background most of the time, so the average bandwidth is much lower than the traditional camera.

Low Power: Power is only used to process changing pixels in event cameras. At the die level, most cameras use about 10 mW, and some prototypes achieve less than 10 μW. Embedded event-camera systems where the sensor is directly interfaced to a processor have shown system-level power consumption (i.e., sensing plus processing) of 100 mW or less [28] [29] [30].

B. Weaknesses
In addition to the significant advantages, there are also some disadvantages in current applications for event cameras.

Large Noise: Due to the structure of the sensor, event cameras are sensitive to background activity noise caused by transient noise and leakage currents of semiconductor PN junctions. When the light is low or the sensitivity is high, the background activity will increase, and the noise will be more. [31] [32] study denoising for event cameras, and major manufacturers are optimizing their processes to reduce noise.

Large Pixel Size: The pixel size of the current event camera is larger than that of the traditional camera. The pixel size of the event camera shown in Table I is mostly above 10 μm, while that of the traditional industrial camera is about 2~4 μm. The large pixel size results in a relatively small resolution of the event camera.

Small Fill Factor: Fill factor is the ratio of a pixel’s light-sensitive area to its total area. The fill factor of event cameras is commonly small, which means that much pixel area is useless.

https://youtu.be/cffwH41ReF4?si=bpshDkPw-2nFASnd

individual pixels talk to the readout via a request and an acknowledge.
parallel communications by reading separate events across the image? could identify the communication source based on, like a ethernet?

_____


# FSOC
https://ieeexplore.ieee.org/document/1577553 
FSOC wavelength windows - 825nm 1330nm 1550nm 

typical free space loss is 20 dB (for a point to point system)  -- if we can still detect/communicate with a lower loss than we do better than a typical point to point.

Atmospheric loss
This may cause polarization fluctuations, beam steering, image dancing, beam spreading and scintillation. Scintillation causes the amplitude of the received signal to fluctuate rapidly by as much as 30 dB with power spectral density spanning 0.01–200 Hz, and hence give rise to long bursts of data errors.

interconnects on datacenters have started using coherent detection that uses other sensors to extract data. 
however using coherent detection on an event based camera would be difficult so maybe stick with direct detection.

https://community.fs.com/article/100g-metro-data-center-interconnectivity-dci-coherent-vs-direct-detection.html

coherent detection methods
https://ntrs.nasa.gov/api/citations/20200006812/downloads/20200006812.pdf


_____
optical characterisation of the atmosphere
https://ntrs.nasa.gov/api/citations/20190001012/downloads/20190001012.pdf

Considering low earth orbit satellites and optical ground station links
https://onlinelibrary.wiley.com/doi/10.1002/sat.1426
using the water vapor, co2 absorption and other aerosol absorption spectra, a region of wavelengths best suited for this is between 1550nm. close to the optical CLU bands. 
(might be useful to follow the maths and show what is best within the 0 - 10km atmosphere region.) (airplanes fly about 8 - 11km)

testing FSO in a coastal environment to see a derived attenuation coefficient.
https://opg.optica.org/oe/fulltext.cfm?uri=oe-26-6-6614&id=383128
1550nm is the least sensitive wavelength in relative humidity and temperature changes. 
_____


