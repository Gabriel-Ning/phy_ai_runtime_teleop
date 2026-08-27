# Physical AI Runtime Teleop

ROS 2 Jazzy teleoperation input packages for Physical AI Runtime.

## Packages

- `gamepad_teleop`: gamepad-to-Twist and gripper reference input source.
- `piper_leader_teleop`: Piper homomorphic leader input source with explicit
  disabled, shadow, and preempt control states.

The packages are kept independent of robot-specific bringup. Runtime topic
remapping, authority, and controller selection belong in the consuming
workspace's profile and launch configuration.

## Build

Place this repository in a ROS 2 workspace, then run:

```bash
colcon build --packages-select gamepad_teleop piper_leader_teleop
```

`piper_leader_teleop` additionally requires `libpiper` and
`piper_description`.

See each package README for its launch arguments, topics, and state-machine
behavior.

