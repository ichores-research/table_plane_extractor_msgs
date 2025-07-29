cmake_minimum_required(VERSION 2.4.6)
project(table_plane_extractor_msgs)

# Get the information about this package's buildtime dependencies
find_package(catkin REQUIRED
  COMPONENTS 
  message_generation 
  std_msgs 
  sensor_msgs
  vision_msgs
#  actionlib_msgs 
)

# Declare the message files to be built
#add_message_files(
#  FILES
#  Plane.msg
#)

# Declare the service files to be built
add_service_files(FILES
  TablePlaneExtractor.srv
)

# add_action_files(FILES
#   CheckForDetections.action
#   GenericImgProcAnnotator.action
# )

generate_messages(
  DEPENDENCIES
  std_msgs
  sensor_msgs
  vision_msgs
)

# Declare that this catkin package's runtime dependencies
catkin_package(
  CATKIN_DEPENDS 
  std_msgs
  sensor_msgs
  vision_msgs
)