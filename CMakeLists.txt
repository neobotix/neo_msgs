cmake_minimum_required(VERSION 2.8.3)
project(neo_msgs)

## Find catkin macros and libraries
## if COMPONENTS list like find_package(catkin REQUIRED COMPONENTS xyz)
## is used, also find other catkin packages
find_package(catkin REQUIRED COMPONENTS
  std_msgs
  message_generation
)

 ##Generate messages in the 'msg' folder
 add_message_files(
   FILES
    	EmergencyStopState.msg
	Keypad.msg
	LCDOutput.msg
	USBoard.msg
	RelayBoardV2.msg
	IOBoard.msg
 )


 generate_messages(
   DEPENDENCIES
   std_msgs
 )

catkin_package(
  CATKIN_DEPENDS message_runtime
)


