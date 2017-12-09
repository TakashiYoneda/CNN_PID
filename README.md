# CNN_PID

### PID Component

P:  
steering angle should be propotionally adjusted by the distance gap between right truck and current position (vertical distance from line to vehicle position).  With more distance (vehicle is away from target path), with more steep angle (steering angle will be adjusted to make vehicle back to path).

D:  
steering angle should be propotionally adjusted by the distance gap velocity of vehicle (time difference of distance gap).  With faster vertical gap verocity to right path, with more negative steering angle against right path.   

I:
steering angle should be propotionally adjusted by incremented vertical distance gap between right path and vehicle position.  This could happen when vehicle module adjustment (e.g. setting of tire angle) is different from assumed setting under PD control.   


### Final Parameters  

