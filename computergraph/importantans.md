# Important questions and answers

## Unit 1

### Frame Buffer
Each screen pixel corresponds to a perticular entry in a 2d array residing memory. This memory is called a frame buffer or a bit map. The number of rows in the frame buffer equals to the number of raster lines on the display screen.  

The number of columns in this array euals to the number of pixels on each raster line. The term pixel is also used to describe the row and column location in frame buffer array that corresponds to screen location. A pixel memory locations.  

Whenever we wish to display a pixel on the screen, a specific value is placed into the corresponding memory location in the frame buffer array.  

Each screen pixel location and corresponding memory location in the frame buffer is accused bu the non-negative integer co-ordinate(x,y).  

The x-value refers to the columns, y-value refers to row position.  
The origin of this coordinate system is positioned at the bottom left corner of the screen or it is positioned at the upper left corner of the screen.  

![fig1](IMG/frameb1.png) ![fig1](IMG/frameb2.png)




### Aspect ratio

### Pixel
A pixel is the smallest piece of information of an image.
- Pixels are normally arranged in a regular 2D grid, and are often represented using dots or squares.
- Each pixel is a sample of an original image where more samples typically provide a more accurate representation of the original 
- The intensity of each pixel is variable in color system, each pixel usually has 3 or 4 components "RED, GREEN and BLUE" or "CYAN, MAGENTA and YELLOW"

### VGA

### Resolution

### Random scan

### Raster scan

### difference between random and raster scan

### CRT

### Brassenhams line drawing algorithm
Let us consider the line in the fig where P is the previously selected pixels and E and NE are two pixels from which we choose at the next stage. Let Q be the intersection point of the line being scan converted with the grid line ![x=xp+1](https://latex.codecogs.com/gif.latex?x%3Dx_p&plus;1)
![Diagram](IMG/Bresenhamsdiagram.png)  
The difference between vertical distances from E and NE to Q is computed and the sign of the difference is used to select the pixel whose distance from Q is smaller as the best approximation to the line. If the mid point M lies above the line, the pixel E is chosen to the line; if the mid point lies below the line pixel NE is chosen to the line.  
Let us consider the straight line by the equation  
![f(x,y)=ax+by+c=0](https://latex.codecogs.com/gif.latex?f%28x%2Cy%29%3Dax&plus;by&plus;c%3D0..............................%281%29)  

The equation straight line can be written as  
![y=mx+b](https://latex.codecogs.com/gif.latex?y%3Dmx&plus;b)  

![or =\frac{dy}{dx}x+b](https://latex.codecogs.com/gif.latex?or%20%3D%5Cfrac%7Bdy%7D%7Bdx%7Dx&plus;b)  

or ![ydx=xdy+Bdx](https://latex.codecogs.com/gif.latex?ydx%3Dxdy&plus;Bdx)  
or ![xdy-ydx+bdx=0](https://latex.codecogs.com/gif.latex?xdy-ydx&plus;Bdx%3D0.........................................%282%29)  

Comparing 1 and 2, we get  
![a=dy,b=-dx,c=Bdx](https://latex.codecogs.com/gif.latex?a%3Ddy%2C%20b%3D-dx%2C%20c%3DBdx)  

![F(x,y)=0,](https://latex.codecogs.com/gif.latex?F%28x%2Cy%29%3D0%2C) *for points on the straight line*  
![F(x,y)>0,](https://latex.codecogs.com/gif.latex?F%28x%2Cy%29%3E0%2C) *for points below the straight line*  
![F(x,y)<0,](https://latex.codecogs.com/gif.latex?F%28x%2Cy%29%3C0%2C) *for points above the straight line*  
We now consider the decision variable.  
![(x_p+1, y_p+\frac {1}{2})](https://latex.codecogs.com/gif.latex?d%28old%29%3DF%28x_p&plus;1%2C%20y_p&plus;%5Cfrac%20%7B1%7D%7B2%7D%29), [where ![(x_p+1, y_p+\frac {1}{2})](https://latex.codecogs.com/gif.latex?%28x_p&plus;1%2C%20y_p&plus;%5Cfrac%20%7B1%7D%7B2%7D%29) is the co-ordinates of the mid point M]  
![=a(x_p+1)+b(1_p+\frac {1}{2})+c](https://latex.codecogs.com/gif.latex?%3Da%28x_p&plus;1%29&plus;b%281_p&plus;%5Cfrac%20%7B1%7D%7B2%7D%29&plus;c)  

If d>0, we choose the pixel NE  
If d<0, we choose the pixel E  
If d=0, we choose either of the pixels, so we pick E.  
If E is chosen, M is incremented by 1 step in x direction and we get  
![d(new)=F(x_p+2,y_p+\frac {1}{2})](https://latex.codecogs.com/gif.latex?d%28new%29%3DF%28x_p&plus;2%2Cy_p&plus;%5Cfrac%20%7B1%7D%7B2%7D%29)  
![=a(x_p+2)+b(y_p+\frac {1}{2})+c](https://latex.codecogs.com/gif.latex?%3Da%28x_p&plus;2%29&plus;b%28y_p&plus;%5Cfrac%20%7B1%7D%7B2%7D%29&plus;c)  

![d(new)-d(old)=a(x_p+2)+b(y_p+\frac {1}{2})+c-a(x_p+1)-b(y_p+\frac {1}{2})-c=a](https://latex.codecogs.com/gif.latex?d%28new%29-d%28old%29%3Da%28x_p&plus;2%29&plus;b%28y_p&plus;%5Cfrac%20%7B1%7D%7B2%7D%29&plus;c-a%28x_p&plus;1%29-b%28y_p&plus;%5Cfrac%20%7B1%7D%7B2%7D%29-c%3Da)  
If NE is chosen then M is incremented in both x and y directions by 1 unit. In this:  

![d(new)=d(old)+a+b](https://latex.codecogs.com/gif.latex?d%28new%29%3Dd%28old%29&plus;a&plus;b)  
![=F(x_p+2,y_p+\frac {3}{2})](https://latex.codecogs.com/gif.latex?%3DF%28x_p&plus;2%2Cy_p&plus;%5Cfrac%20%7B3%7D%7B2%7D%29)  
![=a(x_p+2)+b(y_p+\frac {3}{2})+c](https://latex.codecogs.com/gif.latex?%3Da%28x_p&plus;2%29&plus;b%28y_p&plus;%5Cfrac%20%7B3%7D%7B2%7D%29&plus;c)  

![d(new)-d(old)=a(x_p+2)+b(y_p+\frac {3}{2})+c-a(x_p+1)+b(y_p+\frac {1}{2})-c=a+b](https://latex.codecogs.com/gif.latex?d%28new%29-d%28old%29%3Da%28x_p&plus;2%29&plus;b%28y_p&plus;%5Cfrac%20%7B3%7D%7B2%7D%29&plus;c-a%28x_p&plus;1%29&plus;b%28y_p&plus;%5Cfrac%20%7B1%7D%7B2%7D%29-c%3Da&plus;b)  
![d(new)=d(old)+a+b](https://latex.codecogs.com/gif.latex?d%28new%29%3Dd%28old%29&plus;a&plus;b)  
Since the first pixel is simply the first end point ![(x_o,y_o)](https://latex.codecogs.com/gif.latex?%28x_o%2Cy_o%29), we can directly calculate the initial value of d for choosing between E and NE.
The first mid point is at  
![(x_o+1,y_o+\frac {1}{2})and\; F(x_o+1,y_o+\frac {1}{2})=a(x_o+1)+b(y_o+\frac {1}{2})+c](https://latex.codecogs.com/gif.latex?%28x_o&plus;1%2Cy_o&plus;%5Cfrac%20%7B1%7D%7B2%7D%29and%5C%3B%20F%28x_o&plus;1%2Cy_o&plus;%5Cfrac%20%7B1%7D%7B2%7D%29%3Da%28x_o&plus;1%29&plus;b%28y_o&plus;%5Cfrac%20%7B1%7D%7B2%7D%29&plus;c)  
![=ax_o+a+by_o+\frac {b}{2}+c](https://latex.codecogs.com/gif.latex?%3Dax_o&plus;a&plus;by_o&plus;%5Cfrac%20%7Bb%7D%7B2%7D&plus;c)  
![=ax_o+by_o+c+a+\frac {b}{2}](https://latex.codecogs.com/gif.latex?%3Dax_o&plus;by_o&plus;c&plus;a&plus;%5Cfrac%20%7Bb%7D%7B2%7D)  
![a+\frac {b}{2}](https://latex.codecogs.com/gif.latex?%5Csmall%20%3Da&plus;%5Cfrac%20%7Bb%7D%7B2%7D%5C%3B%20%5B%5Cbecause%20%28x_o%2Cy_o%29is%5C%2C%20on%5C%2C%20the%5C%2C%20straight%5C%2C%20line%5C%2C%20ax&plus;by&plus;c%3D0%5C%2C%20we%5C%2C%20get%5C%2C%20ax_o&plus;by_o&plus;c%3D0%5D)  

Thus, ![d(start)=F(x_0+1,y_o+\frac {1}{2})=a+\frac {b}{2}=dy-\frac{dx}{2}](https://latex.codecogs.com/gif.latex?%5Csmall%20d%28start%29%3DF%28x_0&plus;1%2Cy_o&plus;%5Cfrac%20%7B1%7D%7B2%7D%29%3Da&plus;%5Cfrac%20%7Bb%7D%7B2%7D%3Ddy-%5Cfrac%7Bdx%7D%7B2%7D)  
Using ![d(start)](https://latex.codecogs.com/gif.latex?%5Csmall%20d%28start%29), we can choose the 2nd pixel and so on.  
To eliminate the fraction in ![d(start)](https://latex.codecogs.com/gif.latex?%5Csmall%20d%28start%29), we define the original equation ![F(x,y)=0](https://latex.codecogs.com/gif.latex?%5Csmall%20F%28x%2Cy%29%3D0) by multiplying it by 2, ie, ![F(x,y)=2(ax+by+c)](https://latex.codecogs.com/gif.latex?%5Csmall%20F%28x%2Cy%29%3D2%28ax&plus;by&plus;c%29)  
This multiplies each constant and the decision variable by 2, but does not effect the sign of the decision variable.


### DDA line drawing algorithm

### Brassenhams Circle drawing algo

### Polygon filling algorithm

### Boundary filling algorithm



## Unit 2

### 2d transformation

### homogeneous coordinate

### graphic premitive

### window port & view port

### clipping and sheilding

### 3d display system


## Unit 3

### Spline

### Bspline

### Qubick spline
