# Spaceflight Mechanics - Interplanetary Trajectory Design

Some files not here, notably need to find/remake figure of merit, vehicle params, and atmospheric EDL blocks
(wip - I recently discovered my old usb drive from grad level coursework, figured I'd throw them here)

For whats currently in repo: 

Classical_to_Cartesian_Orbital_Element_Converter.m user may input classical orbital elements to convert to cartesian positions and first rates of change about three axes.

Cartesian_to_Classical_Orbital_Element_Convertor.m converts user inputed cartesian values to classical orbital elements

Transfers.m parses through planetary ephemeris data and plots first order approximations for orbital transfers using lamberts TOF equations. Script intakes Julian Start and Julian arrival dates for whatever timeframe mission is desired. This specific script only applies to an Earth/Mars Interplanetary Direct Transfer (aka no VEEGA, Multi-Assist style trajectories), using patched conic method about the three spheres of influence (Earth-Centric, Helio-Centric, Mars-Centric) and plots specific energies to accomidate planetary transfers. 

ephem.m and lambert_solver.m are given functions where:

ephem.m pulls and propagates JPL spice data from a .mat file

lambert_solver.m solves Lambert's Problem using Battin's method where user inputs two position vectors, the estimated time of flight, grafitational parameters, and some boundry values for numerical solver.

EDL where art thou... 

Side note to anyone viewing, I have some commented out values and/or hard coded inputs for altering missions that aren't very dynamic in its current implementation:
ex one off: "mumoon = 398600;" %Gravitational Parameter of Earth (km^3/s^2)  (aka don't use this code as a black box and expect good results) 

Lunar Parking orbit to Mars Transfer C3 Pork Chop Plotted over 2 Synodic Periods 
<img width="1008" height="595" alt="Moon to Mars C3" src="https://github.com/user-attachments/assets/d2a9190c-7ebb-45d3-96ff-f9adde60a7c7" />

Mars Atmospheric Entry Plot
<img width="1008" height="543" alt="Atmospheric Entry Velocity" src="https://github.com/user-attachments/assets/c072159e-ecc8-4044-89e9-276d563a2ae2" />
