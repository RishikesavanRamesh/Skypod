FROM osrf/ros:humble-desktop

# Install additional ROS packages and dependencies as needed
RUN apt-get update && apt-get install -y \
    emacs 

# Set up a colcon workspace
RUN mkdir -p /colcon_ws/src
WORKDIR /colcon_ws
RUN /bin/bash -c "source /opt/ros/$ROS_DISTRO/setup.bash && colcon build"
RUN echo "source /colcon_ws/install/setup.bash" >> /root/.bashrc
