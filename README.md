# CNN_PID

### PID Component

P:  
steering angle should be propotionally adjusted by the distance gap between right truck and current position (vertical distance from line to vehicle position).  With more distance (vehicle is away from target path), with more steep angle (steering angle will be adjusted to make vehicle back to path).

D:  
steering angle should be propotionally adjusted by the distance gap velocity of vehicle (time difference of distance gap).  With faster vertical gap verocity to right path, with more negative steering angle against right path.   

I:  
steering angle should be propotionally adjusted by incremented vertical distance gap between right path and vehicle position.  This could happen when vehicle module adjustment (e.g. setting of tire angle) is different from assumed setting under PD control.   


### Final Parameters  

Adjustment Process:  
- 1: Set PID parameters with zeros   
vehicle just run straight and out of course   

- 2: (P) adjustment to 0.1   
vehicle fall out from path with first curve around lake because of wider ocillation 

- 3: (D) adjustment to 0.1  
vehicle ocillation became slightly narrower. then increased to 1.0 then 2.0 then 5.0.   
vehicle's ocillation became narrow, but since recovery steering is late especially at the last two corners.   

- 4: (P) adjustment to 0.12   
recovery steering is still late especially at the last two corners, then increased to 0.14 then 0.18   
vehicle succeeded to path final two steep corners, but on the last mild left curve vehicled ocillated.  

- 5: (D) adjustment to 6.0
vehicle still ocillated on the last mild left curve, then up to 8.0.  
succeeded to run through without fail.  

- 6: (I) small adjustment  
vehicle's i_error was accumulated then set I parameter to offset i_error.



