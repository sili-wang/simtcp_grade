### Usage of grade script

You may want to test your result with grade.py, this script can be run in terminal by the following line:

python3 grade.py


My python version is python 3.8. You need to modify line 28 if you have a different python version.
We have 10 testcase, the grade script will gives you the total transimision time and the number of success case.




### Writing Your Solution

This repo contains several tools that will help you simulate and test your
solution.  **You should not make changes to any file other than `project.py`.**
All other files contain code used to either simulate the unreliable connection,
or code to help you test your your solution.

Your solution `project.py` file will be tested against stock versions of all the
other files in the repo, so any changes you make will not be present at
grading time.

Your solution must be contained in the `send` and `recv` functions in `project.py`.
You should not change the signatures of these functions, only their bodies.
These functions will be called by the grading script, with parameters
controlled by the grading script.  Your solution must be general, and should
work for any file.

Your task is to modify the bodies of these functions so that they communicate
using a protocol that ensures that the data sent by the `send` function
can be reliably and quickly reconstructed by the `recv` function.  You should
do so through a combination of setting timeouts on socket reads (e.x.
`socket.timeout(float)`) and developing a system through which each side can
acknowledge if / when they receive a packet.

Remember that the connection is bandwidth constrained.  No more than two
packets can be "on the wire" at a time. If you send a third packet while
there are already two packets traveling to their destination (in either
direction), the third packet will be dropped, so it is important that you get
your timeouts and your acknowledgments right.



### Acknowledgement

This course project is originally developed by Prof. Chris Kanich and Prof. Brent Stephens in their networking class: https://www.cs.uic.edu/~ckanich/cs450/s18/homework5.html. Thank them for sharing the respository to start with!
