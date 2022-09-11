
# Pseudocode Project
## Describing how an elevator works
### Objects/INIT
1. Elevator
   - Goes up and down while listening for updates in an array
    - When it's recieved a number from the array it detects what floor it needs to go too then it determines whether or not to go up or down. When it has completed all of items in the array it stops.

2. Button Panels
   - Button Panel Inside
     - Has (open door) and (close door) buttons. On press the buttons push a number to an array where the  
   - Button Panel Outside
     - calls the elevator to it's location and adds to the queue.
   - Button
     - on press it sends it's floor number to the 

3. Door
   - opens when arrived on a floor that had a button press on the outside or inside
     - Also closes when a button has been pressed on the inside unless open door button is being pressed
### Functions

1. callElevator()
   * Outside Panel only
   * Tells the elevator to go to the floor of the item in the queue
2. checkCurrentFloor()
   * chekcs what current floor the elevator is on // THIS IS A MAYBE (and see whether or not it needs to go up or down) //dont know if this will corectly work.
3. DoorOpen()
   * Opens the door whenever the elevator is on the same floor as an item in queue.
4. findRidersFloor()
   * tells the elevator what floor the rider called the elevator from and adds it to an array with .push
5. stopAtFloor()
   * once the elevator reached the item in the queue or goes to a floor with a called elevator input.
6. buttonPress
   * when the button us pressed it tells the elevator what floor the press was executed on.

~~~
let riderPickupQueueUp []
let riderPickupQueueDown []

Function callElevator
      WHEN a button has been pressed (buttonPress)
         
Function stopAtFloor
      IF elevatorFloor = a floor inside riderPickupQueueUp
         open all doors and continue up
      ELSE IF elevatorFloor = a floor inside riderPickupQueueDown
         open all doors and continue down
Function buttonPress
      IF the button's floor > elevatorFloor
         ADD the buttons floor value to the riderPickupQueueUp
      ELSE IF button's floor < elevatorFloor 
         ADD the buttons floor value to the riderPickupQueueUp
      ELSE do nothing
~~~
