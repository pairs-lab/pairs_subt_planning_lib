# pairs_subt_planning_lib

A C++ path-planning library for PAIRS UAVs operating in cluttered, GPS-denied environments such as subterranean spaces. It provides a 3D grid A* planner that searches over an occupancy map built from point clouds and octomaps, producing collision-free paths for the autonomy stack to follow. The package is a header-and-library only (no ROS nodes); other PAIRS components link against it.

## Contents

- `PairsSubtPlanningLib_Planner` — shared library (`pairs_subt_planning` namespace) built from:
  - `astar_planner` — 3D A* search over an octomap grid with obstacle-distance cost terms.
  - `pcl_map` (`PCLMap`) — loads maps from PCD/octomap and answers nearest-obstacle distance queries using PCL.

## Branches
- `ros1` — ROS 1 Noetic (catkin)
- `ros2` — ROS 2 Jazzy (ament_cmake)

## Install (ROS 2 Jazzy)
```bash
sudo apt install ros-jazzy-pairs-subt-planning-lib
```

## License
BSD 3-Clause. Derived from the CTU-MRS `pairs_subt_planning_lib` package; the original
copyright is retained in [LICENSE](LICENSE).
