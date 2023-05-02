Download Link: https://assignmentchef.com/product/solved-computer-graphics-lab-assignment-3
<br>






+ 2020_ITE0000_2019000001

+ LabAssignment2/

+ 1/

<ul>

 <li>py</li>

</ul>

+ 2/

<ul>

 <li>py</li>

</ul>

+ 3/

<ul>

 <li>py</li>

</ul>




<ul>

 <li>The submission time is determined not when the commit is made but when the git push is made.</li>

</ul>




<ol>

 <li>Write down a Python program to draw a rotating triangle.</li>

 <li>Set the window title to <strong>your student ID</strong> and the window size to (480,480).</li>

 <li>Draw a triangle using render() function below (DO NOT modify it!).</li>

</ol>

<strong>def</strong> render<strong>(</strong>T<strong>):</strong>

glClear<strong>(</strong>GL_COLOR_BUFFER_BIT<strong>)</strong>     glLoadIdentity<strong>()</strong>     # draw cooridnate     glBegin<strong>(</strong>GL_LINES<strong>)</strong>     glColor3ub<strong>(</strong>255<strong>,</strong> 0<strong>,</strong> 0<strong>)</strong>     glVertex2fv<strong>(</strong>np<strong>.</strong>array<strong>([</strong>0.<strong>,</strong>0.<strong>]))</strong>     glVertex2fv<strong>(</strong>np<strong>.</strong>array<strong>([</strong>1.<strong>,</strong>0.<strong>]))</strong>     glColor3ub<strong>(</strong>0<strong>,</strong> 255<strong>,</strong> 0<strong>)</strong>     glVertex2fv<strong>(</strong>np<strong>.</strong>array<strong>([</strong>0.<strong>,</strong>0.<strong>]))</strong>     glVertex2fv<strong>(</strong>np<strong>.</strong>array<strong>([</strong>0.<strong>,</strong>1.<strong>]))</strong>

glEnd<strong>()</strong>

# draw triangle glBegin<strong>(</strong>GL_TRIANGLES<strong>)</strong>

glColor3ub<strong>(</strong>255<strong>,</strong> 255<strong>,</strong> 255<strong>)</strong>

glVertex2fv<strong>( (</strong>T @ np<strong>.</strong>array<strong>([</strong>.0<strong>,</strong>.5<strong>,</strong><strong>1.</strong><strong>]))[:-</strong><strong>1</strong><strong>] )</strong>     glVertex2fv<strong>( (</strong>T @ np<strong>.</strong>array<strong>([</strong>.0<strong>,</strong>.0<strong>,</strong><strong>1.</strong><strong>]))[:-</strong><strong>1</strong><strong>] )</strong>     glVertex2fv<strong>( (</strong>T @ np<strong>.</strong>array<strong>([</strong>.5<strong>,</strong>.0<strong>,</strong><strong>1.</strong><strong>]))[:-</strong><strong>1</strong><strong>] )</strong>     glEnd<strong>()</strong>




<ol>

 <li>Expected result: Uploaded LabAssignment3-1.mp4</li>

</ol>

<table width="371">

 <tbody>

  <tr>

   <td width="36"><strong>Key </strong></td>

   <td width="335"><strong>Transformation </strong></td>

  </tr>

  <tr>

   <td width="36">W</td>

   <td width="335">Scale by 0.9 times in x direction</td>

  </tr>

  <tr>

   <td width="36">E</td>

   <td width="335">Scale by 1.1 times in x direction</td>

  </tr>

  <tr>

   <td width="36">S</td>

   <td width="335">Rotate by 10 degrees counterclockwise</td>

  </tr>

  <tr>

   <td width="36">D</td>

   <td width="335">Rotate by 10 degrees clockwise</td>

  </tr>

  <tr>

   <td width="36">X</td>

   <td width="335">Shear by a factor of -0.1 in x direction</td>

  </tr>

 </tbody>

</table>

<ol>

 <li>Do not mind the initial angle of the triangle.</li>

 <li>The triangle should be t rad rotated when t seconds have elapsed since the program was executed.</li>

 <li>You need to somehow combine a rotation matrix and a translation matrix to produce the expected result.</li>

 <li>Files to submit: A Python source file (Name the file whatever you want (in English). Extension should be .py)</li>

</ol>




<ol start="2">

 <li>Write down a Python program to draw a transformed triangle.</li>

 <li>Set the window title to <strong>your student ID</strong> and the window size to (480,480).</li>

 <li>Draw a triangle using render() function of prob 1 (DO NOT modify it!).</li>

 <li>If you press or repeat a key, the triangle should be transformed as shown in the Table:</li>

</ol>

<table width="370">

 <tbody>

  <tr>

   <td width="36">C</td>

   <td width="334">Shear by a factor of 0.1 in x direction</td>

  </tr>

  <tr>

   <td width="36">R</td>

   <td width="334">Reflection across x axis</td>

  </tr>

  <tr>

   <td width="36">1</td>

   <td width="334">Reset the triangle with identity matrix</td>

  </tr>

 </tbody>

</table>

<ol>

 <li>Transformations should be accumulated (composed with previous one) unless you press ‘1’.</li>

 <li>Be sure: gComposedM = newM @ gComposedM</li>

 <li>You’ll need to make ‘gComposedM’ as a global variable.</li>

 <li>Files to submit: A Python source file (Name the file whatever you want (in English).</li>

</ol>

Extension should be .py)