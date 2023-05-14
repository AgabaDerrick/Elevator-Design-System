# Elevator-Design-System
A console application in Java using OOP principles that simulates the movement of elevators.
An elevator has the following behaviours:
When an elevator is going up or down, it will stop at all the floors that the users requested.
If the elevator received a request of going down while it is going up, the elevator will go to the highest floor in the current requests, and then go down.
Users can send requests at anytime.
Although the elevator needs to sort the requests by some kind of order. It’s not by timestamp, because if elevator is at floor 1, and customer A wants to go to floor 4, and customer B wants to go to floor 2, the elevator should not go to floor 4 first just because A sent the request first. Instead, the elevator should stop at floor 2 and let customer B out, then go to floor 4 to let A out. Thus, the request is sorted by the distance from the current floor and not by timestamp.
Take a scenario if a person is on a particular floor. Suppose Ground Floor. He/She wants to go to 5th Floor. So he clicks on the elevator button with up direction.
This will be called the ExternalRequest. This Request will be having the direction and the floor on which the button has been pressed by the user i.e. source floor. The elevator will check the available requests if any and then process this request depending on some priority. The elevator reaches the source floor i.e. the ground floor. The person enters the elevator.
The person enters the elevator. The person then presses the 5th floor button in the elevator to indicate the elevator to go to 5th floor.
This will be the internal request. So the internal request will be having only the floor to which the person wants to go to i.e. the destination floor. The elevator moves to the fifth floor. And the person then exits the elevator.
If suppose when the elevator is moving from the ground floor to the fifth floor and it reaches the first floor. At this moment suppose another person on the second floor wants to go in the UP direction. Then the elevator will stop for this request and the person on second floor will enter the elevator. Suppose he presses the 4th floor button. Then the elevator will first stop at 4th floor which was the destination of the person which entered on the second floor. Later the elevator stops on the fifth floor and the person from the ground floor exits.
If suppose when the elevator is moving from the ground floor to the fifth floor and it reaches the first floor. At this moment suppose another person on the second floor want’s to go in the DOWN direction. Then the elevator will not stop for this request immediately. Elevator will first go to the fifth floor where the person from the ground floor will exit. Elevator will then go to the second floor. The person will enter the elevator and press 0. The elevator will then move to the zeroth floor.
