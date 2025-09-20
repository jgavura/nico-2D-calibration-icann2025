# NICO 2D Calibration

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.17167890.svg)](https://doi.org/10.5281/zenodo.17167890)


Calibration of NICO for sim-to-real transfer in 2D tasks. Win/Linux friendly.

## Instalation

You need just numpy and pybullet

`pip install pybullet`


If you want to work with real robot, you need to install NicoMotion

https://github.com/knowledgetechnologyuhh/NICO-software/tree/master/api/src/nicomotion

`python setup.py`


## How to use

**Basic test**

`python ik_solver.py`

It has to output 7 joint angles in radians in repetitive manner

**Visualization**

`python ik_solver.py -g`

There is robot randomly calculating IK for finger on the line

**Left/right hand switch**

`python ik_solver.py -g -l`

The IK solver switch to left hand

**Custom position**
`python ik_solver.py -g -p 0.4 -0.3 0.3`

It will repeatedly calculate IK for this position and output joint angles to terminal

**Reset to initial position**

`python ik_solver.py -g -i`

It will reset robot to initial position after each calculation

**Animate motion**

`python ik_solver.py -g -a`

It will show the trajectory of motion in simulator

**Real robot**

`python ik_solver.py -g -rr`

It will initialize robot to default position and then execute the motion from IK

**Custom movements**

If you want to put custom trajectory or other methods (from x,y,z to joint angles) write it to the target method instead of random generator
