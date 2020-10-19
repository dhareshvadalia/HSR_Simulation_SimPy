<H1>London-Birmingham HSR Simulation and Optimization</H1>

<b>INTRODUCTION</b><br>
Simulation process is designed determine the throughput of trains running between 4 stations (London Euston to Birmingham Cruzon) on HSR line for 60 min. High Speed trains never run in perfect ideal scenario, various extrenal factors impacts the speed and movement of the train in real world scenario. Strong winds heavily impacts overall traveling time of High Speep trains [4], which makes it an imparotant factor to be considered while designing the simulation for High speed trains. In Refernce with Beaufort wind force scale [5] values 5-10 is selected. Using the values of this impact factor is calculated, overall which will affect the movement of trains in HSR line. Also, variablity in dwell time is considered which is caused due to fluctuation in movement of passangers.
alt text
ASSUMPTIONS
As stated in problem statement, minimum 2 blocks distance should be maintanined. As a train can run constantly at full speed if there is always at least one free block ahead. Also, train is only allowed to enter a block, when there is no other train in the block and the entry signal is green. When a train enters a block the entry signal switches to red. The entrance signal switches back to green 5 seconds after the end of the train has left the block.<br>
HIGH SPEED TRAIN DETAILS\ \ max speed = 83.3 m/s (300 km/hr)\ 0 - 300 km/h
acceleration = 0.72 m/s^2\ distance = 4820 m\ time = 115.7 s
300 - 0 km/h
deceleration = 0.36 m/s^2 (Energy optimal deceleration)\ distance = 9640 m\ time = 231.4 s
<b>OBJECTIVE<b><br>
Part 1: Simulation Objectives<br>
To create a simulation for the London-Birmingham section of the high-speed line under assumption of a number k of signalling blocks.
Depending on the number of signalling blocks simulate the throughput of trains.<br>
Part 2: Optimization Objectives<br>
Determine K optimal number of blocks and N optimal number of trains (Kopt,Nopt)<br>
Minimise the overall average traveling time<br>
Maximise the throughput of passengers in peak hours.<br>
