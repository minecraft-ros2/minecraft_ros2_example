# minecraft_ros2_example

## LiDAR SLAM

![lidarslamimage](/images/lidarslam.jpg)

### Prerequisites
- minecraft_ros2
- ros2 humble

### Setup

```bash
git clone https://github.com/kazu-321/minecraft_ros2_example.git
cd minecraft_ros2_example
vcs import src < example.repos
rosdep install -y --from-paths src --ignore-src --rosdistro $ROS_DISTRO
colcon build --symlink-install --cmake-args -DCMAKE_BUILD_TYPE=Release
```

## Run

```bash
# Terminal 1
cd ~/minecraft_ros2
source ./install/setup.bash
ros2 launch minecraft_ros2_example lidarslam_ros2.launch.xml
```

```bash
# Terminal 2
cd ~/minecraft_ros2
./runClient.sh
```