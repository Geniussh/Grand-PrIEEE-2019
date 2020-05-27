# UCSD Grand PrIEEE (Line Following Robot) Competition 2019, Team 5

The full documentation can be found at [Team 5 Documentation](https://drive.google.com/file/d/1QUnVXjLTIUAFoJQuONkuO3ktRH37gFut/view)

Two functions were implemented to enable the robot to follow the line and finish the competition. 
* Find the center of the line (a white tape in the non-white background)
  * Filter the input from the linescan camera
  * Determine the gradients across pixels
* Detect the finish line
  * Determine if the number of gradients over the threshold is more than if there were just one line
  * Then simply set the motor speed to zero

The loop for completing the race is
* Capture frame
* Calculate center of line
* Feed the error into PID constants
* Set servo angle accordingly from feedback control
