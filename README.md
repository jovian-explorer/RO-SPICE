The following code helps the user to get the geometries involved in an RO experiment without having to go through the trouble of learning SPICE. The user just needs to load the kernels of the bodies in question in their study, change the names and dates accordingly, and get the desired values in the form of a csv. This script calculates various geometric properties related to an occultation experiment involving a probe, a target object, and an observer. It uses the SPICE toolkit from NASA's Navigation and Ancillary Information Facility (NAIF) to perform the calculations. This script is not only applicable for Solar occultation experiments, but can also be applied for planetary atmosphere occultation studies as well.

### Prerequisites:
- The SPICE toolkit from NAIF must be installed and available in the system's PATH.
- The kernel files containing the necessary SPICE data must be provided.


### Input:
The script requires the following inputs:

- The name or NAIF code of the probe.
- The name or NAIF code for the object of study (target).
- The name or NAIF code of the observing station.
- The length of the observation period in seconds.
- The number of parts to divide each second into (subdivisions per second).
- Mass of the target body in question (Has to be added in the code itself, may/may not add a functionality for removing this input).

### Output:
The script calculates all geometric properties for an occultation experiment for each time step in the observation period:

- The state of the probe and the observer in the Solar System barycentric (SSB) frame.
- The velocity of the probe and the observer in the SSB frame.
- The position of the probe and the observer in the SSB frame, normalized to astronomical units (AU).
- The distance between the probe and the observer.
- The distance between the point of closest approach and t
- The angular separation between the probe and the observer, as seen from the target.
- The angular separation between the target and the observer, as seen from the probe.
- The script also generates a Pandas DataFrame containing the calculated geometric properties and saves it to a CSV file.
