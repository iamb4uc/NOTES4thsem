# Unit 2

### Two Dimensional Viewing

#### 2D Transformation

##### Basic Transformation:

 With the procedures for displaying output primitive and their attributes, we can create a variety of pictures and graphics. In many application, there is also a need for altering or manipulating displays. Design application and facility layouts are created by arranging the orientations and sizes of the component parts of the scene and orientations are produced by moving the camera or the objects in a scene along animation path changes in orientations size and shape are accomplished with geometric transformations that alter the coordinate description of objects.  
There are three types of transformations:  
1. **Translation**: A translation is applied to an object by repositioning it along a straight line path from one coordinate locations to another.  
![before translation](IMG/btranslation.png) ![after translation](IMG/atranslation.png)  
The equation of translation is given by,  
![x'=x+h etc](https://latex.codecogs.com/svg.latex?%5Cinline%20%5Clarge%20%5Cleft.%5Cbegin%7Bmatrix%7D%20x%27%3Dx+h%5C%5Cy%27%3Dy+k%20%5Cend%7Bmatrix%7D%5Cright%5C%7D................................................%281%29)  
Where p'(x',y') is the new co-ordinate for the points p(x,y) by applying addition to x and y co-ordinates with h and k quality. In matrix form (1) can be written as:  
![\\begin{bmatrix}x'\\y' \\end{bmatrix} =\\begin{bmatrix}h\\k \\end{bmatrix} + \\begin{bmatrix}x\\y\\end{bmatrix}](https://latex.codecogs.com/svg.latex?%5Cinline%20%5Clarge%20%5Cbegin%7Bbmatrix%7D%20x%27%5C%5Cy%27%20%5Cend%7Bbmatrix%7D%20%3D%5Cbegin%7Bbmatrix%7D%20h%5C%5Ck%20%5Cend%7Bbmatrix%7D%20+%20%5Cbegin%7Bbmatrix%7D%20x%5C%5Cy%20%5Cend%7Bbmatrix%7D)  
or  
![P'=T+P..................(1)](https://latex.codecogs.com/svg.latex?%5Cinline%20%5Clarge%20P%27%3DT+P..................%281%29) where ![](https://latex.codecogs.com/svg.latex?%5Cinline%20%5Clarge%20T%20%3D%20%5Cbegin%7Bbmatrix%7D%20h%5C%5C%20k%20%5Cend%7Bbmatrix%7D) is the translation matrix.  

2.  **Scaling**: A scaling transformation alters the size of an object. This operation can be carried for polygons by multiplying the co-ordinates value(x,y) of each vertex by scaling factors by ![S\_\_x\\; and\\; S\_\_y](https://latex.codecogs.com/svg.latex?%5Cinline%20%5Clarge%20S__x%5C%3B%20and%5C%3B%20S__y) to produce the transformed co-ordinates.  
    ![diagram](IMG/scale.png)  
    Points can be scaled (or stretched) by ![S\_\_x\\; and\\; S\_\_y](https://latex.codecogs.com/svg.latex?%5Cinline%20%5Clarge%20S__x%5C%3B%20and%5C%3B%20S__y) along x and y axis respectively, then the new co-ordinates can be obtained as  
    ![](https://latex.codecogs.com/svg.latex?%5Cinline%20%5Clarge%20%5Cleft.%5Cbegin%7Bmatrix%7D%20x%27%3DS__xx%5C%5C%20y%27%3DS__yy%20%5Cend%7Bmatrix%7D%5Cright%5C%7D............................................%282%29)  
    In matrix form equation (2) can be written as  
    ![](https://latex.codecogs.com/svg.latex?%5Cinline%20%5Clarge%20%5Cbegin%7Bbmatrix%7D%20x%27%5C%5Cy%27%20%5Cend%7Bbmatrix%7D%3D%5Cbegin%7Bbmatrix%7D%20S__x%20%26%200%5C%5C%200%20%26%20S__y%20%5Cend%7Bbmatrix%7D+%5Cbegin%7Bbmatrix%7D%20x%27%5C%5Cy%3B%20%5Cend%7Bbmatrix%7D)  
    or  
    ![P'=S\*P.......................(2)](https://latex.codecogs.com/svg.latex?%5Cinline%20%5Clarge%20P%27%3DS*P.......................%282%29) where ![](https://latex.codecogs.com/svg.latex?%5Cinline%20%5Clarge%20S%3D%5Cbegin%7Bbmatrix%7D%20S__x%20%26%200%5C%5C%200%20%26%20S__y%20%5Cend%7Bbmatrix%7D) is the sealing matrix.  

3.  **Rotation**: A two dimensional rotation is applied to an object by repositioning it along a circular path in the XY plane. To generate a rotation we specify. a rotation angle (-) and the position ![(x_r,y_r)](https://latex.codecogs.com/svg.latex?%5Cinline%20%5Clarge%20%28x_r%2Cy_r%29) of the rotation point about which the object is to be rotated.  
    ![Before Rotation](IMG/brotate.png) ![After rotation](IMG/arotate.png)  
    Points can be rotated through an angle D about the origin R is described by:  
    ![\\left.\\begin{matrix}x'=xcos\\Theta-ysin\\Theta \\y'=xsin\\Theta+ycos\\Theta\\end{matrix}\\right}](https://latex.codecogs.com/svg.latex?%5Cinline%20%5Clarge%20%5Cleft.%5Cbegin%7Bmatrix%7Dx%27%3Dxcos%5CTheta-ysin%5CTheta%20%5C%5Cy%27%3Dxsin%5CTheta+ycos%5CTheta%5Cend%7Bmatrix%7D%5Cright%5C%7D.................%283%29)
    ![diagram](IMG/rotatn.png)  
    Fig: Rotation of an object through angle D about the rotation point ![(x_r,y_r)](https://latex.codecogs.com/svg.latex?%5Cinline%20%5Clarge%20%28x_r%2Cy_r%29)  
    The equation (3) can be written as:  
    ![formula](https://latex.codecogs.com/svg.latex?%5Cinline%20%5Clarge%20%5Cbegin%7Bbmatrix%7D%20x%27%5C%5C%20y%27%20%5Cend%7Bbmatrix%7D%20%3D%20%5Cbegin%7Bbmatrix%7D%20cos%5CTheta%20%26%20-sin%5CTheta%5C%5C%20sin%5CTheta%20%26%20cos%5CTheta%20%5Cend%7Bbmatrix%7D%20%5Cbegin%7Bbmatrix%7D%20x%5C%5C%20y%20%5Cend%7Bbmatrix%7D)  
    or ![](https://latex.codecogs.com/svg.latex?%5Cinline%20%5Clarge%20P%27%3DR%28%5CTheta%29*P.....................%283%29%5C%3Bwhere%5C%3B%20R%28%5CTheta%29%3D%5Cbegin%7Bbmatrix%7D%20cos%5CTheta%20%26%20-sin%5CTheta%20%5C%5C%20sin%5CTheta%20%26%20cos%5CTheta%20%5Cend%7Bbmatrix%7D)  
    Note:  
    ![Note](IMG/note.png)  
    From the triangle OPM, we see that  
    ![formula](https://latex.codecogs.com/svg.latex?%5Cinline%20%5Clarge%20sin%5Calpha%3D%5Cfrac%20%7By%7D%7Br%7D%5C%5C%20%7B%5Ccolor%7BRed%7D%20or%7D%5C%3B%20r%5C%2Csin%5Calpha%20%3D%20y%5C%5C%20%5CRightarrow%20y%3Dr%5C%2C%20sin%5Calpha%20%5C%5C%20cos%5Calpha%3D%5Cfrac%20%7Bx%7D%7Br%7D%5C%5C%20%7B%5Ccolor%7BRed%7D%20or%7D%5C%3B%20r%5C%2C%20cos%5Calpha%20%3D%20x%20%5C%5C%20%5CRightarrow%20x%20%3Dr%5C%2C%20cos%5Calpha%5C%5C%5C%5C%20From%5C%3B%20%5Cbigtriangleup%20OP%27M%27%5C%3B%20we%5C%3B%20see%5C%3B%20that%5C%5C%20sin%28%5CTheta+%5Calpha%29%3D%5Cfrac%20%7By%27%7D%7Br%7D%5C%5C%20%5CRightarrow%20y%27%3Dr%5C%2C%20sin%28%5CTheta+%5Calpha%29%5C%5C%5C%5C%20%7B%5Ccolor%7BRed%7D%20Similarly%7D%2C%5C%5C%20cos%28%5CTheta+%5Calpha%29%3D%5Cfrac%20%7Bx%27%7D%7Br%7D%5C%5C%20%5CRightarrow%20x%27%3Dr%5C%2C%20cos%28%5CTheta+%5Calpha%29%5C%5C%5C%5C%20%7B%5Ccolor%7BRed%7D%20Now%7D%2C%5C%5C%20x%27%3Dr%5C%3Bcos%28%5CTheta+%5Calpha%29%5C%5C%20%3Dr%28cos%5CTheta*cos%5Calpha-sin%5CTheta*sin%5Calpha%29%5C%5C%20%5Cbegin%7Bmatrix%7D%20%3Dr%5C%2Ccos%5Calpha*cos%5CTheta-r%5C%2Csin%5Calpha*sin%5CTheta%20%26%20%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%5BS_y*x%3Dr%5C%2Ccos%5Calpha%5D%20%5C%5C%20%3Dx*cos%5CTheta-y*sin%5CTheta%20%26%20%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%5BS_x*y%3Dr%5C%2Csin%5Calpha%5D%20%5Cend%7Bmatrix%7D%5C%5C%20y%27%3Dr%5C%2Csin%28%5CTheta+%5Calpha%29%5C%5C%20%3Dr%28sin%5CTheta*cos%5Calpha+cos%5CTheta*sin%5Calpha%29%5C%5C%20%3Dr%5C%3Bsin%5CTheta*cos%5Calpha+r%5C%3Bcos%5CTheta*sin%5Calpha%5C%5C%20%3Dr%5C%3Bsin%5CTheta+y%5C%3Bcos%5CTheta)  <!-- sin\alpha=\frac {y}{r}\\
    {\color{Red} or}\; r\,sin\alpha = y\\
    \Rightarrow y=r\, sin\alpha \\
    cos\alpha=\frac {x}{r}\\
    {\color{Red} or}\; r\, cos\alpha = x \\
    \Rightarrow x =r\, cos\alpha\\\\
    From\; \bigtriangleup  OP'M'\; we\; see\; that\\
    sin(\Theta+\alpha)=\frac {y'}{r}\\
    \Rightarrow y'=r\, sin(\Theta+\alpha)\\\\
    {\color{Red} Similarly},\\
    cos(\Theta+\alpha)=\frac {x'}{r}\\
    \Rightarrow x'=r\, cos(\Theta+\alpha)\\\\
    {\color{Red} Now},\\
    x'=r\;cos(\Theta+\alpha)\\
    =r(cos\Theta*cos\alpha-sin\Theta*sin\alpha)\\
    \begin{matrix}
    =r\,cos\alpha*cos\Theta-r\,sin\alpha*sin\Theta & \;\;\;\;\;\;\;\;\;\;[S_y*x=r\,cos\alpha] \\
    =x*cos\Theta-y*sin\Theta & \;\;\;\;\;\;\;\;\;\;[S_x*y=r\,sin\alpha]
    \end{matrix}\\
    y'=r\,sin(\Theta+\alpha)\\
    =r(sin\Theta*cos\alpha+cos\Theta*sin\alpha)\\
    =r\;sin\Theta*cos\alpha+r\;cos\Theta*sin\alpha\\
    =r\;sin\Theta+y\;cos\Theta -->  
    Note:
    The matrix represented for scaling, translation and rotation are respectively.  
    ![](https://latex.codecogs.com/svg.latex?%5Cinline%20%5Clarge%20%5C%5C%20P%27%3DS*P..............................%281%29%5C%5C%20P%27%3DT+P.............................%282%29%5C%5C%20P%27%3DR*P..............................%283%29)  
    where translation is in the form of addition but scaling and rotation is in the form of multiplication. We would like to be able to treat all these transformation in a consistent way as multiplication.  

##### <u>Homogeneous co-ordinate</u>

In homogeneous co-ordinate we add a third co-ordinate to a point(x,y) each point. Instead of being represented by tripple (x,y,w). At the same time we see that two sets of co-ordinates (x,y,w) and (x',y',w') represent the same point if and only if one is multiple of other.  
Also, atleast one of the homogeneous co-ordinate must be non-zero(0,0,0) is not allowed. If w != 0, we can divide the point (x,y,w) by w and we get(x/w,y/w,1). But (x,y,w) and (x/w,y/w,1) represent the same point. The points with w = 0 are called points of infinity.  

###### Translation in homogeneous co-ordinate

The equation of translation (1) can be written as:  
![equation](https://latex.codecogs.com/svg.latex?%5Cinline%20%5Clarge%20%5Cbegin%7Bbmatrix%7D%20x%27%5C%5C%20y%27%5C%5C%201%20%5Cend%7Bbmatrix%7D%20%3D%20%5Cbegin%7Bbmatrix%7D%201%20%26%200%20%26%20dx%20%5C%5C%200%20%26%201%20%26%20dy%5C%5C%200%260%261%20%5Cend%7Bbmatrix%7D%5Cbegin%7Bbmatrix%7D%20x%5C%5C%20y%5C%5C%201%20%5Cend%7Bbmatrix%7D)  
Here,  
h = dx = displacement along x-axis.  
k = dy = displacement along y-axis.  
or,  
P' = T(dx, dy)P..........................(I')  
![](https://latex.codecogs.com/svg.latex?%5Cinline%20%5Clarge%20%7B%5Ccolor%7BRed%7D%20where%7D%5C%3B%20%5C%3B%20T%28dx%2Cdy%29%3D%5Cbegin%7Bbmatrix%7D%201%20%26%200%20%26%20dx%5C%5C%200%20%26%201%20%26%20dy%5C%5C%200%20%26%200%20%26%201%20%5Cend%7Bbmatrix%7Dis%20%5C%3B%20the%5C%3B%20translation%5C%3B%20matrix.)  

###### Scaling in Homogeneous co-ordinate:
In homogeneous co-ordinate, the two dimensional scaling matrix will be  
![equation](https://latex.codecogs.com/svg.latex?%5Cinline%20%5Clarge%20%5Cbegin%7Bbmatrix%7D%20x%27%5C%5C%20y%27%5C%5C%201%20%5Cend%7Bbmatrix%7D%3D%5Cbegin%7Bbmatrix%7D%20S_x%20%26%200%20%26%200%5C%5C%200%20%26%20S_y%20%26%200%5C%5C%200%260%261%20%5Cend%7Bbmatrix%7D%5Cbegin%7Bbmatrix%7D%20x%5C%5C%20y%5C%5C%201%20%5Cend%7Bbmatrix%7D%5C%5C%20or%2C%5C%5C%20P%27%3DS%28S_x%2CS_y%29P...............................%28II%29%5C%5C%20Where%2C%5C%5C%20S%28S_x%2CS_y%29%3D%5Cbegin%7Bbmatrix%7D%20S_x%20%26%200%20%26%200%5C%5C%200%20%26%20S_y%20%26%200%5C%5C%200%260%261%20%5Cend%7Bbmatrix%7D%5C%2C%20is%5C%2C%20the%5C%2C%20scaling%5C%2C%20matrix)  

###### Rotation in Homogeneous co-ordinate:
The equation of rotation can be written as:  
![equation](https://latex.codecogs.com/svg.latex?%5Cinline%20%5Clarge%20%5Cbegin%7Bbmatrix%7D%20x%27%5C%5C%20y%27%5C%5C%201%20%5Cend%7Bbmatrix%7D%3D%5Cbegin%7Bbmatrix%7D%20cos%5CTheta%20%26%20-sin%5CTheta%20%26%200%5C%5C%20sin%5CTheta%20%26%20cos%5CTheta%20%26%200%5C%5C%200%260%261%20%5Cend%7Bbmatrix%7D%5Cbegin%7Bbmatrix%7D%20x%5C%5C%20y%5C%5C%201%20%5Cend%7Bbmatrix%7D%5C%5C%20or%2C%5C%5C%20P%27%3DR%28%5CTheta%29*P.........................%28III%29%5C%5C%20Where%2C%5C%5C%20R%28%5CTheta%29%3D%5Cbegin%7Bbmatrix%7D%20cos%5CTheta%20%26%20-sin%5CTheta%20%26%200%5C%5C%20sin%5CTheta%20%26%20cos%5CTheta%20%26%200%5C%5C%200%260%261%20%5Cend%7Bbmatrix%7D%5C%2C%20is%5C%2C%20the%5C%2C%20rotational%5C%2C%20matrix)  
