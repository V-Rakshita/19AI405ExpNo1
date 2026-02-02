<h1>ExpNo 1 :Developing AI Agent with PEAS Description</h1>
<h3>Name: V RAKSHITA</h3>
<h3>Register Number/Staff Id: 212224100049</h3>


<h3>AIM:</h3>
<br>
<p>To find the PEAS description for the given AI problem and develop an AI agent.</p>
<br>
<h3>Theory</h3>
<h3>Smart Home Temperature Control Agent:</h3>
<p>This agent monitors the temperature in a room and adjusts it to maintain an optimal range (18°C to 26°C). The environment consists of one or more rooms in a house. The agent senses the current temperature in a room and decides whether to turn on the heater or air conditioner. The performance of the agent is measured by how well it maintains the temperature within the optimal range while minimizing unnecessary actions. Hence, the agent continuously monitors and adjusts the room temperature efficiently.</p>

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
    <td>Smart Home Temperature Control Agent</td>
    <td>Maintain optimal temperature, minimize unnecessary heating/cooling</td>
    <td>Rooms in a house</td>
    <td>Heater, air conditioner</td>
    <td>Room temperature sensor</td>
  </tr>
</table>

<hr>
<h3>DESIGN STEPS</h3>
<h3>STEP 1: Identifying the input:</h3>
<p>Current temperature of the room.</p>
<h3>STEP 2: Identifying the output:</h3>
<p>Turn on heater if temperature is below 18°C, turn on air conditioner if temperature is above 26°C, do nothing if temperature is optimal.</p>
<h3>STEP 3: Developing the PEAS description:</h3>
<p>PEAS description is developed by identifying the performance measure, environment, actuators, and sensors used by the agent.</p>
<h3>STEP 4: Implementing the AI agent:</h3>
<p>The agent monitors the room temperature continuously and adjusts it by turning on the heater or air conditioner as needed.</p>
<h3>STEP 5:</h3>
<p>Measure the performance parameters: Performance improves when the room temperature is maintained within the optimal range, and unnecessary actions (turning on heater or AC when not needed) reduce performance.</p>


<H3>Program:</H3>

```python
import random
import time

class SmartHomeAgent:
    def __init__(self, home_data):
        self.home_data = home_data

    def monitor_temperature(self):
        while True:
            current_temp_state = self.sensors.get_temperature_state()
            action = self.choose_action(current_temp_state)
            self.actuators.perform_action(action)
            # Wait a bit before the next reading to simulate continuous monitoring
            time.sleep(2)

    def choose_action(self, current_temp_state):
        temperature = current_temp_state['temperature']
        if temperature < 18:
            return "Turn on heater"
        elif temperature > 26:
            return "Turn on air conditioner"
        else:
            return "Temperature is optimal"

class TemperatureSensors:
    def get_temperature_state(self):
        # Simulate temperature readings
        return {
            'temperature': random.uniform(15.0, 30.0)
        }

class TemperatureActuators:
    def perform_action(self, action):
        print(action)

if __name__ == "__main__":
    home_data = {'home_id': 101, 'name': 'Green Villa'}
    
    temp_sensors = TemperatureSensors()
    temp_actuators = TemperatureActuators()
    
    smart_home_agent = SmartHomeAgent(home_data)
    smart_home_agent.sensors = temp_sensors
    smart_home_agent.actuators = temp_actuators
    
    smart_home_agent.monitor_temperature()
```
<h3> Output:</h3>

<img width="362" height="494" alt="image" src="https://github.com/user-attachments/assets/95dd7168-5309-4cff-9855-63bc7352978e" />
