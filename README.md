# Table Top Pong board

## The Idea
A while ago I saw a video of a pong like board that had space for four players and thought it would make a fun project. The video showed a table top game that involved players controller paddles using controllers used to bounce a ball in an attempt to score on the oponents net. This table top game appeared to use solenoids activated by buttons on the players controller to allow the ball to bounce off the paddles. 

One problem that was displayed in the video was the flat board. The players had to constantly touch the ball with their hands since it would sometimes stop moving the middle of the board.

My twist would be to make the game only two player and add a slope in the middle of the board, making it so the ball doesn't get stuck and require player intervention. It would also be interesting to add different power ups. For example, maybe an electromagnet that could be activated to "catch" the ball on the field.

## Implementation
I came across the CH32V003 which seemed like a good fit for the controllers since they are very cheap. Because of their simple function I believe they would be a good fit and allow me to venture out of the mode widely used micro controllers (Raspberry Pi Pico, Arduino, ESP32). Don't get me wrong, I am likely going to use a Pico or an ESP32 for the game board to allow for hassle free usage of FreeRTOS to manage the game.

## MVP
The minimum viable prototype is two controllers and a game board. The paddles should be driven by a motor to allow them to move back and forward and there should be a solenoid on board to enable the shoving action. The board should be constructed in such a way that the ball used as the game ball does not get stuck.

## Extra features
Having a scoreboard and some powerups would also be cool.

## Expected Challenges
Mechanical Design: My CAD knowledge is quite limited, so I believe that paddle mechanisms may be a challenge to design.

Driving Motors: I have never worked with stepper motors before, but I am hoping that some limit switches and some stepper motors that have encoders will help make things easier.

Complex PCB design: With this being my second entry in PCB design I am worried about the complexity of driving the various voltages and currents with steppers and solenoids. I am hopping that I don't need individual driver motors for each paddle, but it is entirely possible that I will. At this point, I am hoping to have a 2 layer PCB for the controllers, and a 4 layer PCB for the baord. Fingers crossed I don't also need mottor driver boards for the paddles.
