cmake_minimum_required(VERSION 3.5.0)

project(romi-soss-ros2)

find_package(soss-rosidl REQUIRED)
find_package(soss-ros2 REQUIRED)
find_package(rmf_dispenser_msgs REQUIRED)
find_package(rmf_door_msgs REQUIRED)
find_package(rmf_fleet_msgs REQUIRED)
find_package(rmf_lift_msgs REQUIRED)
find_package(rmf_task_msgs REQUIRED)
find_package(building_map_msgs REQUIRED)

soss_rosidl_mix(
  PACKAGES
    rmf_dispenser_msgs
    rmf_door_msgs
    rmf_fleet_msgs
    rmf_lift_msgs
    rmf_task_msgs
    building_map_msgs
  MIDDLEWARES
    ros2
)