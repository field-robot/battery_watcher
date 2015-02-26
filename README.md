# battery_watcher

##New user
- Do first ros tutorial
- Make account on github
- `gedit .bashrc`
  - Add this to the bottom of the file:
  - ```source ~/catkin_ws/devel/setup.bash```

- Type this in terminal
  - `git config -- global user.email “sameemailasgithub”`
  - `git config -- global user.name “My Name”`
  - `git config -- global push.default simple`







## Creating a new package.

- Create repository on github/field-robot (for example battery_watcher)
- Go to the directory where all ros packages are:
  - `cd ~/catkin_ws/src`
- Download the package you just created
  - `git clone https://github.com/field-robot/battery_watcher.git` (this address can be found on the github webpage)
- Make an actual package of it
  - `catkin_create_pkg battery_watcher std_msgs rospy roscpp`
- Check if you can 'make' the package
  - `cd ~/catkin_ws`
  - `catkin_make`
- Upload the new files to github
  - Go the directory first
    - `roscd battery_watcher`
  - Tell git which new files you have
    - `git add CMakeList.txt`
    - `git add package.xml`
  - Check if it went allright
    - `git status`
  - Then commit the files
    - `git commit -am “I just created this package”`
  - Then upload to github
    - `git push`
  - Other users can now get these changes as follows:
    - `roscd battery_watcher`
    - `git pull`





## Changing a package
- Change the package
- Check if the packages builds
  - `cd ~/catkin_ws`
  - `catkin_make`
- See which files have changed:
  - `roscd battery_watcher`
  - `git status`
- If this is right, you can commit the changes
  - `git commit -am “I changed something, make this a usefull message”`
- And then upload it to the server
  - `git push`
