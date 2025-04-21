<h1>ExpNo 1 :Developing AI Agent with PEAS Description</h1>
<h3>Name: MOHAMED ZABIR KHAN A</h3>
<h3>Register Number: 212224230162</h3>


<h3>AIM:</h3>

<p>To find the PEAS description for the given AI problem and develop an AI agent.</p>


<h3>Theory</h3>

<p>Performance Measure: minimize energy consumption, maximize dirt pick up. Making this precise:
one point for each clean square over lifetime of 1000 steps.

Environment: two squares, dirt distribution unknown, assume accions are deterministic and
environment is static (clean squares stay clean).

Actuators: Left, Right, Suck, NoOp.

Sensors: agent can perceive its location and whether location is dirty.</p>

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
    <td><strong>Vaccum Cleaner</strong></td>
    <td><strong>Cleanliness, Number of Movements</strong></td>
     <td><strong>Rooms, Dust</strong></td>
    <td><strong>Steering, Cleanliness</strong></td>
    <td><strong>Location, Motion</strong></td>
  </tr>
</table>

## DESIGN STEPS
### STEP 1:
Identifying the input:
### STEP 2:
Identifying the output:
### STEP 3:
Developing the PEAS description:
### STEP 4:
Implementing the AI agent
### STEP 5:
Measure the performance parameters


## PROGRAM

class VacuumCleanerAgent:
    def __init__(self):
        # Initialize the agent's state (location and dirt status)
        self.location = "A"  # Initial location (can be "A" or "B")
        self.dirt_status = {"A": False, "B": False}  # Initial dirt status (False means no dirt)

    def move_left(self):
        # Move the agent to the left if possible
        if self.location == "B":
            self.location = "A"

    def move_right(self):
        # Move the agent to the right if possible
        if self.location == "A":
            self.location = "B"

    def suck_dirt(self):
        # Suck dirt in the current location if there is dirt
        if self.dirt_status[self.location]:
            self.dirt_status[self.location] = False
            print(f"Sucked dirt in location {self.location}")

    def do_nothing(self):
        # Do nothing
        pass

    def perform_action(self, action):
        # Perform the specified action
        if action == "left":
            self.move_left()
        elif action == "right":
            self.move_right()
        elif action == "suck":
            self.suck_dirt()
        elif action == "nothing":
            self.do_nothing()
        else:
            print("Invalid action")

    def print_status(self):
        # Print the current status of the agent
        print(f"Location: {self.location}, Dirt Status: {self.dirt_status}")

# Example usage:
agent = VacuumCleanerAgent()

# Move the agent, suck dirt, and do nothing

agent.perform_action("left")
agent.print_status()
agent.perform_action("suck")
agent.print_status()
agent.perform_action("nothing")
agent.print_status()



# OUTPUT

![Screenshot 2024-02-27 133811](https://github.com/subikshan2006/19AI405ExpNo1/assets/139841805/210720af-15a6-47a5-acc4-65f62579e7c3)


# RESULT
Thus, an AI agent is developed.
