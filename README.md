# wbc

* 3rd_party : Contain 3rd party libs, such as boost, eigen, and yaml-cpp etc.
* rthread(Robotics-THREAD) : Implement UDP connection, shared memory, and timer event. Also, named mutex is included. Depends on 3rd parties.
* rmath(Robotics-MATH) : Wrapper and helper functions/classes of anything about math calculation.
* kinematics : Parse yml file, and calculate Jacobians and forward kinematics. Depends on 3rd parties.
* wbc: Calculate desired torques or joint angles/displacements based on an operational space control. Depends on 3rd parties and kinematics.
* examples: Contains sample yml files and codes for wbc. Depends on 3rd parties, xthreads, kinematics and wbc.
