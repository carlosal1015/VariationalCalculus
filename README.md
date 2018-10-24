# VariationalCalculus
Variational Calculus using Minimization. 
Minimization is implemetned by "Minimization.hpp", which you can get from my other repository. 
Variational Calculus is to find a function that gives minimal cost functional (function of function).
The following is an example of cost functional of function <img src="https://latex.codecogs.com/gif.latex?y(x)" />
.

<div align="center">
<img src="https://latex.codecogs.com/gif.latex?F(y(x))=\int_{x_1}^{x_n}y(x)^2+\alpha\left(\frac{\mathrm{d}y}{\mathrm{d}x}\right)^2dx" />
</div>

In this library, we will express a function by a long vector <img src="https://latex.codecogs.com/gif.latex?y_1,\cdots,y_n" />, which is the value corresponding to each x, i.e. <img src="https://latex.codecogs.com/gif.latex?x_1,\cdots,x_n" />. The above example functional can be calculated by the below approximation:

<div align="center">
<img src="https://latex.codecogs.com/gif.latex?F(y(x))\simeq\sum_{i=1}^{n}y_i^2+\alpha\sum_{i=1}^{n-1}\left(y_{i+1}-y_i\right)^2" />
</div>

Now, it is easy to find the solution that gives the minimal of the above left functional, by minimization the above right approximated function, whose variables are <img src="https://latex.codecogs.com/gif.latex?y_1,\cdots,y_n" />.

<div align="center">
<img src="https://latex.codecogs.com/gif.latex?\min_{y_1,...,y_n}\left(\sum_{i=1}^{n}y_i^2+\alpha\sum_{i=1}^{n-1}\left(y_{i+1}-y_i\right)^2\right)" />
</div>


Variational calculus often has some additional constraints. For example, <img src="https://latex.codecogs.com/gif.latex?f(0)=0" />. This can be implemented by using constrainted minimization.

<div align="center">
<img src="https://latex.codecogs.com/gif.latex?F(y(x))\simeq\sum_{i=1}^{n}y_i^2+\alpha\sum_{i=1}^{n-1}\left(y_{i+1}-y_i\right)^2" />
</div>
