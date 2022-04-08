<h1>Introduction</h1> 
After COVID-19 hit the world, there had to be a restriction imposed on the number of people present in one place. 
Moreover, a lot of time is wasted waiting for one’s turn in the bank. 
One solution to these problems is to have a queue management system, where the client is assigned a number and served accordingly. This way, the client does not have to be on site the whole waiting time, and can go do anything meanwhile (finish other errands, go do some work, etc…)
<br>
This project aims at implementing a miniature bank token generator using ATMega32 microcontroller.
The token generator should act as a bank queue management system, where there is a given number of tellers, and clients are served according to the number displayed above each teller.
<h1>Implementation Overview</h1>
<h3>Using <b> LCDs, LEDs, buzzers, push buttons, and ATMega32</b> for controlling the token generator, the queue should be managed as follows:</h3>
1. There are three tellers.<br>
2. Each teller is represented with an LCD.<br>
3. The LCDs will be connected to the microcontroller, and each will have a corresponding LED and a push-down button.<br>
4. When a teller’s button is pressed, the buzzer will go off and the LED will flash for 30 seconds indicating the wait for the next client.<br>
5. If the button is pressed again within these 30 seconds, the LED will stop flashing indicating that the client is now being served.<br>
6. Else, the number on the LCD will be automatically incremented by 1 more than the most recent client being served among the other tellers.<br>
7. Example: If client #3 misses their turn on teller 2, and client #4 is being served at teller 1, and client #5 at teller 3, then teller 2 
will call for client #6.<br>

<h1>Implementation Details</h1>
<h3>Using ATMEL Studio, the code for the microcontroller will be written as follows:</h3>
1. Each LCD will have six pins assigned to it.<br>
2. Each LED will have one pin assigned to it.<br>
3. Each push button will have one pin assigned to it.<br>
4. The buzzer will also have one pin assigned to it.<br>
5. Write a function to start generating the tokens incrementally through checking the maximum client number being currently served, handle the LED flashing, and check the status of the push buttons.
<h1>Future Work</h1>
For further extension of this project, there can be implemented an HTTP API for the queue monitoring, where the client can follow the URL to check the current client number being served using <b>ESP8266 WiFi Module</b>.
