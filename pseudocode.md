# Pseudocode Project
## Describing how an elevator works.
### Objects
1. Elevator
    * when it's recieved an number form the array it dettects what floor it needs to go too then it determines whether or not to go up or down. When it has completed all of items in the array it stops.
2. Door
    * opens when arrived on a floor that had a button press on the outside and inside
    * Also closes when a button has been pressed on the inside unless open door button is being pressed
3. Button Panels
  * Button Panel Inside
    * Has (open door) and (close door) buttons. Also has an array of buttons that tell the elevator where to go/what function to call.
  * Button Panel Outside
    * calls the elevator to it's location and adds to the queue.
### procedure for picking up a person
~~~
START
INIT = power on

WHILE power on 
    check queue for items
    check current floor of the elevator
---
WHEN outside input button is pressed
    create input
    add input to the queue
---

---
IF the queue has more than 0 in the array
    check what floor number it is
ELSE IF inputs floor > elevator's current floor
    go up
ELSE
    go down
ELSE
    stay still
---    
IF inputs floor location is a number higher than the position of the elevator
    go "up"
ELSE
    go "down
---   
IF going "up"
    check closest input between current floor and max floor
---    
IF going "down"
    check closest input between current floor and minimum floor
---   
WHEN reached the queues current item 
    open doors
    reset input button
    check inside input
    delete floors input
--- 
// When the elevator has someone on it.

WHEN the inside button input is pressed
    add input to the queue
    If button input floor > elevator floor
        go up
    ELSE 
        go down
---

~~~
