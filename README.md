# This work has been presented at IROS 2021
Link:

https://ieeexplore.ieee.org/abstract/document/9635859

Citation:

@INPROCEEDINGS{9635859,
author={Cursi, Francesco and Bai, Weibang and Kormushev, Petar},
booktitle={2021 IEEE/RSJ International Conference on Intelligent Robots and Systems (IROS)},
title={Kalibrot: A Simple-To-Use Matlab Package for Robot Kinematic Calibration}, 
year={2021},
volume={},
number={},
pages={8852-8859},
doi={10.1109/IROS51168.2021.9635859}}

# Kalibrot
Algorithm for Robot Kinematic Calibration

- Kalibrot is an optimization algorithm for solving the problem of finding the optimal DH parametres for correct robot kinematc calibration.
- The algorithm uses derivatives of the Cartesian position and orientation (computed through quaternions) which are retrieved analytically, thus speeding up the computations.
- Two different methods can be used: 
    1) traditional **pseudoinverse**;
    2) **constarined quadratic programming** problem (solved using quadprog from matlab).

## Functions
The main functions are:
- `getModel.m` which solves the optimization problem. It finds the optimal DH parameters and also outputs additional information such as the identifiable parameters or the observability measures;
- `RobotKinematics.m` is a class building the Robot object which allows to compute the forward kinematics and the derivatives wrt DH parameters. It just takes as input the number of joints, their types, and the initial transfromation matrix.
- `VisualizeResults.m` generates three plots for showing the calibrate DH parameters, the calibrated robot kinematic structure, and the identification matrix;
- The others are just auxiliary functions.

### Tests
The `tests` folder contains two examples:
- calibration  of a 3R robot;
- calibration of a Stanford manipulator (6DOF);
- calibration of a KUKA manipulator (7DOF).

- `getData_3R.m`, `getData_Stanford.m`, `getData_Kuka.m` are used to generate the calibration data for the three simulated robots.

### Tutorial
`tutorial.pdf` explains Kalibrot functionalities and how to use it.

### Contact
If you have any question and want to contribute to the project, please email `cursifrancesco@gmail.com` .
We thank you for your interest and help.

### Licensing:
MIT License

Copyright (c) 2024 Francesco Cursi

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

