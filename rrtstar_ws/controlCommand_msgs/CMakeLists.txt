cmake_minimum_required(VERSION 2.8.3)
project(controlCommand_msgs)

find_package(catkin REQUIRED COMPONENTS geometry_msgs message_generation std_msgs )

add_message_files(
  DIRECTORY msg
  FILES
  transformation.msg
  bimanual.msg
  armControl.msg
  Gripper.msg
  stop.msg
  holdMode.msg
  control.msg
  controlTaskParam.msg
  controlGoalReachAck.msg
	singleArmTransportation.msg
)

generate_messages(DEPENDENCIES geometry_msgs std_msgs )

catkin_package(CATKIN_DEPENDS geometry_msgs message_runtime std_msgs  )
