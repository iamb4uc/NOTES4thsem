# Unit 2
### Two Dimensional Viewing
#### 2D Transformation
##### Basic Transformation:
 With the procedures for displaying output primitive and their attributes, we can create a variety of pictures and graphics. In many application, there is also a need for altering or manipulating displays. Design application and facility layouts are created by arranging the orientations and sizes of the component parts of the scene and orientations are produced by moving the camera or the objects in a scene along animation path changes in orientations size and shape are accomplished with geometric transformations that alter the coordinate description of objects.  
There are three types of transformations:  
1. **Translation**: A translation is applied to an object by repositioning it along a straight line path from one coordinate locations to another.  
![before translation](IMG/btranslation.png) ![after translation](IMG/atranslation.png)  
The equation of translation is given by,  
![x'=x+h etc](https://latex.codecogs.com/svg.latex?%5Cinline%20%5Clarge%20%5Cleft.%5Cbegin%7Bmatrix%7D%20x%27%3Dx&plus;h%5C%5Cy%27%3Dy&plus;k%20%5Cend%7Bmatrix%7D%5Cright%5C%7D................................................%281%29)  
Where p'(x',y') is the new co-ordinate for the points p(x,y) by applying addition to x and y co-ordinates with h and k quality. In matrix form (1) can be written as:  
![\begin{bmatrix}x'\\y' \end{bmatrix} =\begin{bmatrix}h\\k \end{bmatrix} + \begin{bmatrix}x\\y\end{bmatrix}](https://latex.codecogs.com/svg.latex?%5Cinline%20%5Clarge%20%5Cbegin%7Bbmatrix%7D%20x%27%5C%5Cy%27%20%5Cend%7Bbmatrix%7D%20%3D%5Cbegin%7Bbmatrix%7D%20h%5C%5Ck%20%5Cend%7Bbmatrix%7D%20&plus;%20%5Cbegin%7Bbmatrix%7D%20x%5C%5Cy%20%5Cend%7Bbmatrix%7D)  
or  
![P'=T+P..................(1)](https://latex.codecogs.com/svg.latex?%5Cinline%20%5Clarge%20P%27%3DT&plus;P..................%281%29) where ![](https://latex.codecogs.com/svg.latex?%5Cinline%20%5Clarge%20T%20%3D%20%5Cbegin%7Bbmatrix%7D%20h%5C%5C%20k%20%5Cend%7Bbmatrix%7D) is the translation matrix.  

2. **Scaling**: A scaling transformation alters the size of an object. This operation can be carried for polygons by multiplying the co-ordinates value(x,y) of each vertex by scaling factors by ![S__x\; and\; S__y](https://latex.codecogs.com/svg.latex?%5Cinline%20%5Clarge%20S__x%5C%3B%20and%5C%3B%20S__y) to produce the transformed co-ordinates.  
![diagram](IMG/scale.png)  
Points can be scaled (or stretched) by ![S__x\; and\; S__y](https://latex.codecogs.com/svg.latex?%5Cinline%20%5Clarge%20S__x%5C%3B%20and%5C%3B%20S__y) along x and y axis respectively, then the new co-ordinates can be obtained as  
![](https://latex.codecogs.com/svg.latex?%5Cinline%20%5Clarge%20%5Cleft.%5Cbegin%7Bmatrix%7D%20x%27%3DS__xx%5C%5C%20y%27%3DS__yy%20%5Cend%7Bmatrix%7D%5Cright%5C%7D............................................%282%29)  
In matrix form equation (2) can be written as  
![](https://latex.codecogs.com/svg.latex?%5Cinline%20%5Clarge%20%5Cbegin%7Bbmatrix%7D%20x%27%5C%5Cy%27%20%5Cend%7Bbmatrix%7D%3D%5Cbegin%7Bbmatrix%7D%20S__x%20%26%200%5C%5C%200%20%26%20S__y%20%5Cend%7Bbmatrix%7D&plus;%5Cbegin%7Bbmatrix%7D%20x%27%5C%5Cy%3B%20%5Cend%7Bbmatrix%7D)  
or  
![P'=S*P.......................(2)](https://latex.codecogs.com/svg.latex?%5Cinline%20%5Clarge%20P%27%3DS*P.......................%282%29) where ![](https://latex.codecogs.com/svg.latex?%5Cinline%20%5Clarge%20S%3D%5Cbegin%7Bbmatrix%7D%20S__x%20%26%200%5C%5C%200%20%26%20S__y%20%5Cend%7Bbmatrix%7D) is the sealing matrix.  

3. **Rotation**: A two dimensional rotation is applied to an object by repositioning it along a circular path in the XY plane. To generate a rotation we specify. a rotation angle (-) and the position ![(x_r,y_r)](https://latex.codecogs.com/svg.latex?%5Cinline%20%5Clarge%20%28x_r%2Cy_r%29) of the rotation point about which the object is to be rotated.  
![Before Rotation](IMG/brotate.png) ![After rotation](IMG/arotate.png)  
Points can be rotated through an angle D about the origin R is described by:  
![\left.\begin{matrix}x'=xcos\Theta-ysin\Theta \\y'=xsin\Theta+ycos\Theta\end{matrix}\right\}](https://latex.codecogs.com/svg.latex?%5Cinline%20%5Clarge%20%5Cleft.%5Cbegin%7Bmatrix%7Dx%27%3Dxcos%5CTheta-ysin%5CTheta%20%5C%5Cy%27%3Dxsin%5CTheta&plus;ycos%5CTheta%5Cend%7Bmatrix%7D%5Cright%5C%7D.................%283%29)
