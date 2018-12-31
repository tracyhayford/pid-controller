# **PID Controller** 

**Project Goals**


### Compilation
Code compiles without errors with cmake and make.

### Implemention
The algorithms taught in the lessons were used to develop the code with guidance from the Q&A video.

### Reflection

#### Parameter Optimization

##### Effect of each parameter
P – too high causes oscillations; too low & the car doesn’t react to curves quickly enough
I – left at zero; no systematic error observed
D – Minimizes the oscillation; too high can cause erratic steering

##### Parameter manual optimization
These values were chosen manually by a number of iterative steps starting with P = -1.0 and I,D = 0.  As expected, the car steering oscillated and eventually left the road.  P was gradually reduced (-0.75, -0.5 and -0.1) and D added (-0.5, initially) to reduce oscillation.  PID of (-0.1, 0, -0.5) mostly kept the car on the road with minimal oscillation.  However, response in curves was too slow and the car would occasionally drive outside the lanes on sharper curves.  To improve respone in the curves, P was increased while increasing D as well to minimize oscillation.  P of -0.17 provided quick enough response in the curves to keep the car on the road.  D of -2.0 led to erratic steering.  D of -1.5 gave the best performance.

##### Final optimized parameters
P = -0.17
I = 0
D = -1.5

### Simulation
The car drives the entire track without leaving the drivable portion of the track.

### Future Activities
* Use Twiddle or another method to automate the parameter optimization
* Try adjusting the speed to see how that impacts parameter selection
