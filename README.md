Download Link: https://assignmentchef.com/product/solved-mce747-homework-2
<br>
<strong>Problem 1:  </strong>Find the Euler angles equivalent to the following sequence of rotations: Rotx(<em>π/</em>2), Roty(−<em>π</em>) (relative to <em>y</em>0), Roty(<em>π/</em>2) (relative to the current frame) and Rotz(-<em>π/</em>2) (relative to <em>z</em>0). Sketch all frames and verify that the Euler angles for the composite rotation work (if there are multiple solutions, show them all).

<strong>Problem 2:  </strong>Consider the PP robot with spherical wrist shown in Fig. 1. Consider all 3 d.o.f. of the spherical wrist to be concentric (zero lengths between joints).

Figure 1: 5-dof robot with spherical wrist.

Figure 2 shows the sign convention from the angles and their zero references.

Figure 2: 5-dof robot with spherical wrist at the zero angle configuration.

<ol>

 <li>Assign a complete set of coordinate frames following the D-H convention strictly, andinclude a summary table. Sketch all frames. Place the origin of the end effector frame at <em>P</em>.</li>

 <li>List the frame-to-frame homogeneous transformations and write a Matlab programthat finds the world position of any point in the end effector frame given numerical values for the five joint coordinates.</li>

 <li>Verify your solution and code with two “easy” configurations that can be sketched tofind <em>P</em><sup>0 </sup>by inspection:

  <ul>

   <li><em>q</em>1 = 1<em>, q</em>2 = 1<em>, q</em>3 = <em>π, q</em>4 = 0<em>, q</em>5 = <em>π/</em>2</li>

   <li><em>q</em>1 = 1<em>, q</em>2 = −1<em>, q</em>3 = <em>π/</em>2<em>, q</em>4 = <em>π/</em>2<em>, q</em>5 = 0</li>

  </ul></li>

</ol>

Running your code with these values should match the coordinates of <em>P</em><sup>0 </sup>obtained from the sketches.

<ol start="4">

 <li>Add lines to your code so that the world coordinates <em>x</em>0(<em>t</em>)<em>, y</em>0(<em>t</em>) and <em>z</em>0(<em>t</em>) of <em>P</em>(<em>t</em>) are calculated for the following joint coordinate functions:

  <ul>

   <li><em>q</em>1(<em>t</em>) = sin(2<em>t</em>)</li>

   <li><em>q</em>2(<em>t</em>) = cos(<em>t</em>)</li>

   <li><em>q</em>3(<em>t</em>) = <em>t</em></li>

   <li><em>q</em>4(<em>t</em>) = sin(2<em>t</em>)</li>

   <li><em>q</em>5(<em>t</em>) = <em>t</em></li>

  </ul></li>

</ol>

Use <em>t </em>∈ [0<em>, </em>20] with increments <em>δt </em>= 0<em>.</em>01.

<ol start="5">

 <li>Plot <em>x</em>0(<em>t</em>)<em>, y</em>0(<em>t</em>) and <em>z</em>0(<em>t</em>) each versus <em>t</em>.</li>

 <li>Make a 3D plot of the end effector trajectory.</li>

 <li>Make 3 projection plots of the above trajectory: <em>xz, xy </em>and <em>yz </em></li>

 <li>List your code and the transformation function library you used.</li>

</ol>

<strong>Problem 3: </strong>Consider the 4-axis SCARA robot shown in Fig. 3. The spindle at the end of the second link can move vertically and also rotate through 360 degrees, providing two degrees of freedom that can be independently actuated.

Figure 3: 4-dof SCARA robot.

A plasma cutting electrode is attached horizontally at the bottom end of the spindle (see Fig. 4). The electrode rotates and moves up and down with the spindle. The robot will be used to cut a rectangular window on a circular-base cylinder located along the reference position shown in the figure. The cylinder has radius 50 mm, is 100 mm tall and is supported 75 mm above the base of the robot. The electrode must be normal to the circumference of the workpiece during the cut. The electrode will not change length during the operation.

The lower edge of the rectangle starts 10 mm from the base of the cylinder, at the point nearest to the spindle. The window should be 15 mm wide and 40 mm tall. The cut should be completed in 20 seconds.

<ol>

 <li>Assign coordinate frames starting from the information given in Fig. 4 and the dimensions at the end of this document. Use the D-H convention.</li>

 <li>Develop the necessary forward kinematics as Matlab code.</li>

 <li>Consult SHV for the solutions to the inverse kinematics for this robot and make necessary adjustments or simplifications as you see fit.</li>

 <li>It is suggested to solve four separate inverse kinematics problems corresponding to eachedge of the window. Find the mathematical expressions for each of the 3D Cartesian trajectories to be followed, as well as the required end frame orientation and write code to generate them numerically, using a speed that allows the task to be completed in 20 seconds.</li>

 <li>Use exact inverse kinematic formulas to find the four required joint angle histories.</li>

 <li>Verify by feeding your solutions back into the forward kinematics.</li>

 <li>Attempt a direct numerical solution using Corke’s Robotics Toolbox (work in metersto prevent numerical issues).</li>

</ol>

Figure 4: Workpiece and initial electrode position