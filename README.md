# ROS2 Actions Example
This repository contains a ROS2 Actions implementation using Python. It includes:
- `my_robot_interfaces` package → Defines the action interface.
- `actions_py` package → Implements the Action Server & Client.

## 1. Action Definition (`my_robot_interfaces/action/CountUntil.action`)
The `CountUntil` action consists of:
- Goal: Target number & period.
- Result: Reached number.
- Feedback: Current number.

## 2. Count Until Action Server (`actions_py/count_until_server.py`)

ros2 run actions_py count_until_server

The action server `CountUntilServerNode` counts up to the `target_number`, waiting `period` seconds between increments.
- Starts an action server on the topic `count_until`.
- Executes the goal and provides feedback.
- Returns the final reached number when completed.
Run the server:

## 3. Count Until Action Client (`actions_py/count_until_client.py`)

ros2 run actions_py count_until_client

The action client `CountUntilClientNode` sends a goal to the action server.
- Sends a `target_number` and `period` to the server.
- Waits for completion and receives feedback.
- Prints the final result.
Run the client:

# ros2-Actions
