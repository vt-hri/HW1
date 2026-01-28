# HW1

Dylan Losey, Virginia Tech.

In this homework assignment we will record and replay demonstrations on a robot arm.

## Install and Run

```bash

# Download
git clone https://github.com/vt-hri/HW1.git
cd HW0

# Create and source virtual environment
# If you are using Mac or Conda, modify these two lines as shown in [HW0](https://github.com/vt-hri/HW0)
python3 -m venv venv
source venv/bin/activate

# Install dependencies
# If you are using Mac or Conda, modify this line as shown in [HW0](https://github.com/vt-hri/HW0)
pip install numpy pybullet

# Run the script
python main.py
```

### Mac

## Expected Output

Use your keyboard to teleoperate the robot.
See `teleop.py` to understand which keys map to which axis of robot motion.

## Assignment

Here are the main steps:
1. implement a limiter to prevent us from teleoperating robot into the table [even better, keep us in a safe bounding box]
2. implement a script to record the states we mark [use the "toggle" button, need to add some logic prevent duplicates. I think these should be recorded as json, but am open to whatever is easiest]
3. create a script to replay that trajectory [picking one block and placing it on the other]
		[will need to recognize difference between position commands, gripper commands...]
		[maybe rename "main.py" as "record", and then make a "replay".]
4. change the location of one of the blocks; enable the user to take over to fix things
		[during replay, student should think about how they want to "pause" the recorded thing, modify, and resume...
		may need to "skip" the next part of their motion, since modified!]
