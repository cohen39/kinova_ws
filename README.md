# kinova_ws
A catkin workspace for working on manipulation with the kinova gen3. 

### Build
These are modified instructions based on ros_kortex readme: https://github.com/cohen39/ros_kortex/edit/noetic-devel/readme.md

First, install ros dependencies & clone this repo:

    sudo apt install python3 python3-pip
    sudo python3 -m pip install conan
    conan config set general.revisions_enabled=1
    conan profile new default --detect > /dev/null
    conan profile update settings.compiler.libcxx=libstdc++11 default
    git clone https://github.com/cohen39/kinova_ws.git
    cd kinova_ws
    rosdep install --from-paths src --ignore-src -y

Then, build:

    catkin_make
    source devel/setup.bash
