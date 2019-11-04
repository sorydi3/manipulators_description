# Theta-Theta manipulator

The theta-theta manipulator has 2 angular DoFs connected by two links as shown in the next figure.

![](./t1t2.png)

## Simulate Theta-Theta manipulator
To run the package you have to download it inside your `catkin_ws/src` folder. You can use:

```bash
~catkin_ws/src $ git clone https://github.com/narcispr/theta_theta_description.git
```
or just download the ZIP file and uncompress it in `catkin_ws/src` folder. Notice that the name must be `theta_theta_description`!

Once you have the package downloaded it is a good habit run the `catkin_make` command (from the root of your workspace) to check if something has to be compiled or generated.

```bash
~catkin_ws $ catkin_make
```

This package do not contain any piece of code just a URDF file and a launch. To execute it run the following command:

```bash
$ roslaunch theta_theta_description view_theta_theta.launch
```

You can enable or disable the GUI that allows you to move the articulations on the robot by changing the param `<param name="use_gui" value="false"/>` from `false` to `true` in the launch file.

## Kinematics 

### Denavit-Hartenberg parameters 

| DoF  | theta_i | d_i  | a_i​  | alpha_i​ |
| ---- | ------- | ---- | ---- | ------- |
| 1    | theta_1 | 0    | 0.40 | 0       |
| 2    | theta_2​ | 0    | 0.45 | Pi/4    |

###  rTh matrix

![](./docs/rTh.png)

### Inverse kinematics

![](./docs/ik.png)

