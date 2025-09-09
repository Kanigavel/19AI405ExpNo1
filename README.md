<h1>ExpNo 1 :Developing AI Agent with PEAS Description</h1>



<h3>AIM:</h3>
<br>
<p>To find the PEAS description for the given AI problem and develop an AI agent.</p>
<br>
<h3>Theory</h3>
<h3>Medicine prescribing agent:</h3>
<p>Such this agent prescribes medicine for fever (greater than 98.5 degrees) which we consider here as unhealthy, by the user temperature input, and another environment is rooms in the hospital (two rooms). This agent has to consider two factors one is room location and an unhealthy patient in a random room, the agent has to move from one room to another to check and treat the unhealthy person. The performance of the agent is calculated by incrementing performance and each time after treating in one room again it has to check another room so that the movement causes the agent to reduce its performance. Hence, agents prescribe medicine to unhealthy.</p>
<hr>
<h3>PEAS DESCRIPTION:</h3>
<table>
  <tr>
    <td><strong>Agent Type</strong></td>
    <td><strong>Performance</strong></td>
     <td><strong>Environment</strong></td>
    <td><strong>Actuators</strong></td>
    <td><strong>Sensors</strong></td>
  </tr>
    <tr>
    <td><strong>Medicine prescribing agent</strong></td>
    <td><strong>Treating unhealthy, agent movement</strong></td>
     <td><strong>Rooms, Patient</strong></td>
    <td><strong>Medicine, Treatment</strong></td>
    <td><strong>Location, Temperature of patient</strong></td>
  </tr>
</table>
<hr>
<H3>DESIGN STEPS</H3>
<h3>STEP 1:Identifying the input:</h3>
<p>Temperature from patients, Location.</p>
<h3>STEP 2:Identifying the output:</h3>
<p>Prescribe medicine if the patient in a random has a fever.</p>
<h3>STEP 3:Developing the PEAS description:</h3>
<p>PEAS description is developed by the performance, environment, actuators, and sensors in an agent.</p>
<h3>STEP 4:Implementing the AI agent:</h3>
<p>Treat unhealthy patients in each room. And check for the unhealthy patients in random room</p>
<h3>STEP 5:</h3>
<p>Measure the performance parameters: For each treatment performance incremented, for each movement performance decremented</p>
<h3>Delveloping by :<h3>
  <h4>Name : Kanigavel M <h4>
    <h4>Reg.No: 212224240070 <h4>
<H3>Program :</H3>
    
    import random
    num_rooms = 5   
    rooms = [f"Room {i+1}" for i in range(num_rooms)]


    patients = {}
    for room in rooms:
        patients[room] = round(random.uniform(97.0, 102.0), 1)

    performance = 0
    agent_location = rooms[0] 

    def prescribe_medicine(temp):
        """Check if patient is unhealthy and prescribe medicine"""
        return temp > 98.5

    print(" Medicine Prescribing Agent Simulation ")
    print("------------------------------------------------")

    for i, room in enumerate(rooms):
        print(f"\nAgent is in {room}")
        temp = patients[room]
        print(f"Patient temperature: {temp}°F")
    
        if prescribe_medicine(temp):
            print("Patient is unhealthy : Medicine prescribed ")
            performance += 1
        else:
            print("Patient is healthy : No medicine needed ")
    
   
        if i < len(rooms) - 1:
            next_room = rooms[i+1]
            print(f"Agent moving from {room} to {next_room}...")
            performance -= 1
            agent_location = next_room

    print("\n------------------------------------------------")
    print(" Simulation Completed")
    print(f" Final Performance Score: {performance}")

<H3>Output :</H3>
<img width="736" height="744" alt="image" src="https://github.com/user-attachments/assets/d8a41751-4f74-4cfc-a8d2-a0c9b39ba601" />
<h3>Result :</h3>
The Python program for Developing AI Agent with PEAS Description was executed successfully.
