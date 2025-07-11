# Platoon Coordination: Line-of-sight (LOS), Non-LOS & Age-of-Information (AoI)-based CACC 
<b> 1. Line-of-sight_communication_with_platoon_leader <br> (Intersection scenario) </b> <br>
This scenario presents a simulation of vehicle platooning using OMNeT++ and SUMO, where OMNeT++ manages wireless communication based on the DSRC protocol, and SUMO models traffic dynamics. The simulation framework is extended with Veins and PLEXE to enable Cooperative Adaptive Cruise Control (CACC) among platoon vehicles. A platoon comprising fifteen vehicles approaches an intersection with an unobstructed line-of-sight (LOS) link to the platoon leader. There are no buildings or physical obstacles at the corner to impair communication. Each vehicle continuously exchanges Cooperative Awareness Messages (CAMs) containing real-time state information such as position, velocity, and acceleration. The availability of a clear LOS ensures that all vehicles receive timely and accurate updates from the leader. As a result, the platoon executes coordinated braking, maintaining safe inter-vehicle distances throught. 

https://github.com/user-attachments/assets/10c6bece-209f-4906-8c0b-e1b175ed74bb

<b> 2. Non-Line-of-sight_communication_with_platoon_leader <br> (Intersection scenario)</b> <br>
In this scenario, a fifteen-vehicle platoon approaches an intersection where a building at the corner blocks the line-of-sight (LOS) to the platoon leader, while communication with the immediate predecessor remains mostly unobstructed. Since the CACC topology relies on both leader and predecessor data, the obstruction causes packet loss from the leader during deceleration. As a result, platoon members receive stale or outdated information from the leader, leading to incorrect control input computation. This causes unsafe inter-vehicle gaps and ultimately results in collisions within the platoon. The scenario highlights how LOS disruptions to the leader critically affect platoon safety.

https://github.com/user-attachments/assets/9288b730-9ce8-48f9-bddc-495ab1bd004f

<b> 3. AoI-aware CACC for Vehicle Platooning  <br> (Urban map scenario)</b> <br>
This scenario demonstrates a control strategy that improves platoon safety in urban environments where communication with the leader is disrupted. The Age of Information (AoI)-aware CACC uses the freshness of received data to decide which vehicle’s information to use during its control input computation. When packets from the leader are delayed or lost, instead of relying on outdated data, each vehicle selects the most recent and reliable data from upstream vehicles (towards the platoon head). This allows the platoon to maintain safe spacing and avoid collisions, even under poor communication conditions caused by buildings or obstacles.

https://github.com/user-attachments/assets/7eaee705-da46-4e02-8f57-bf7fda95a73c



