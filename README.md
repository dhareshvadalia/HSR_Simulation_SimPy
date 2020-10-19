<H1>London-Birmingham HSR Simulation and Optimization</H1>

<b>INTRODUCTION</b><br>
A high-speed train as planned for the HS2 line from London to Birmingham has an acceleration
of 0.72m/s2, about the same as a commuter train. While the trains can brake in an emergency
at 2.5m/s2, the energy optimal deceleration (using regenerative braking) is 0.36m/s2.
The maximum travelling speed of the train is about 300km/h (83.3m/s). Accelerating from 0
to the maximum speed takes therefore 115.7s during which time the train travels about
4,820m. Slow decelerating takes 231.4s and the distance travelled is 9,640m.
A railway line consists of a sequence of signaling blocks. A train is only allowed to enter a
block, when there is no other train in the block and the entry signal is green. When a train
enters a block the entry signal switches to red. The entrance signal switches back to green 5
seconds after the end of the train has left the block.
Depending on the intended maximum traveling speed there is an optimal distance for setting
a pre-signal. At a maximum travelling speed of the train of 300km/h (83.3m/s) the slow
deceleration takes 231.4s and the train travels 9,640m during this time. In this case the presignal
would be 10km before the actual signal at the end of one block and the entry to the
next. The length of a block should therefore be at least 10km, but to allow a train to achieve
and run as long as possible at full speed, the block length should be at least 1.5x this length.
The control problem is to keep the trains moving at maximum possible speed. If there is a
slight delay in one train it may cause the train in the following block to decelerate, potentially
down to a stop, and then to reaccelerate. This in turn will delay the train thereafter. Just like
the “traffic jam” effect you know from the motorway. A train can run constantly at full speed
if there is always at least one free block ahead. With a block length of 15km that means that
the distance between two trains should be about 30km, at full speed a travelling time of about
6min. This would indicate that one could achieve a maximum schedule of 10 trains per hour.
The new government under Boris Johnson is pushing the development of HS2. The economic
argument is based on a schedule time of 9 trains per hour.<br><br>

<b>SIMULATION LOGIC</b><br>
Create a simulation for the London-Birmingham section of the high-speed line under
assumption of a number k of signalling blocks. A decision on the number of signaling blocks is
required, as the track laying is supposed to start soon. Also a decision on the number of trains
running per hour has to be made.
Depending on the number of signalling blocks simulate the throughput of trains.
Take into account that between Birmingham Interchange and Birmingham Curzon street as
well as between London Old Oak Common and London Euston there will be a practical speed
limit and the traveling times are 5 min between London Euston and London Old Oak Common
(one signalling block) and 9 min between Birhigham Interchange and Birmingham Curzon
Street station (two signalling blocks). Take into account the variability of achievable speeds
due to wind and weather conditions on the stretch between London Old Oak Common and
Birmingham Interchange. Take into account the variability in stop times, i.e. minor delays due
to passenger movements.<br>
London Euston<br>
5 min<br>
London Old Oak Common<br>
31 min<br>
Birmingham Interchange<br>
9 min<br>
Birmingham Curzon Street<br>
The distance between London Old Oak Common Station and Birmingham Interchange Station
is 145km. This could be broken down in up-to 14 blocks. If there are less but longer blocks the
trains could achieve in theory a higher average speed, however the throughput in trains per
hour is smaller.

<br><br>
<b>ASSUMPTIONS</b><br>
As stated in problem statement, minimum 2 blocks distance should be maintanined. As a train can run constantly at full speed if there is always at least one free block ahead. Also, train is only allowed to enter a block, when there is no other train in the block and the entry signal is green. When a train enters a block the entry signal switches to red. The entrance signal switches back to green 5 seconds after the end of the train has left the block.
<br><br>
<b>HIGH SPEED TRAIN DETAILS</b><br>max speed = 83.3 m/s (300 km/hr)<br> <b>0 - 300 km/h</b><br>
acceleration = 0.72 m/s^2<br> distance = 4820 m<br> time = 115.7 s<br>
<b>300 - 0 km/h</b><br>
deceleration = 0.36 m/s^2 (Energy optimal deceleration)<br> distance = 9640 m<br> time = 231.4 s
<br><br>
<b>OBJECTIVE</b><br>
Part 1: Simulation Objectives<br>
To create a simulation for the London-Birmingham section of the high-speed line under assumption of a number k of signalling blocks.
Depending on the number of signalling blocks simulate the throughput of trains.<br>
Part 2: Optimization Objectives<br>
Determine K optimal number of blocks and N optimal number of trains (Kopt,Nopt)<br>
Minimise the overall average traveling time<br>
Maximise the throughput of passengers in peak hours.<br>
