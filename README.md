# Line-Search-Algorithm
 Optimal line search or Exact line search is used for calculating step size for gradient descent. This descent is performed towards the steepest descent direction which is given as follows, 
<p align="center">
 <a href="https://www.codecogs.com/eqnedit.php?latex=\large&space;d&space;=&space;-\frac{\nabla&space;f(\bar{x})}{\left&space;\|\nabla&space;f(\bar{x})&space;\right&space;\|}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\large&space;d&space;=&space;-\frac{\nabla&space;f(\bar{x})}{\left&space;\|\nabla&space;f(\bar{x})&space;\right&space;\|}" title="\large d = -\frac{\nabla f(\bar{x})}{\left \|\nabla f(\bar{x}) \right \|}" /></a> 
</p>

THe difference between Backtracking and Optimal Line Search is that for the former, the step size is incremented or decremented by a variable amount whereas for latter the increment or decrement is set to be constant, here 0.001. 

## Backtracking Line Search Algorithm:

```
1: t=1
2: dx = - df(x')
3: repeat t = b.t
4: until f(x' +t.dx)<f(dx) + a.t.df(x')^Tdx
```

where a is the learning rate and b is the change factor. Step 4 is known as the stopping condition and should be checked for every step. <br>

<p align="center">
  <img src="https://raw.githubusercontent.com/tanishkasingh9/Line-Search-Algorithm/master/Images/tmain.png"> 
  </p>


## Optimal Line Search Algorithm:

```
1: t > 0
2: min = [f(x'); t0]
3: dx = - df(x')
4: for some fixed number of iterations
5: do increment t=stepsize by some constant small value, here 0.001
6: dx = - df(xold)
7: find xnew = xold + t.dx
8: if f(xnew) > min[0] then update min[0] = f(xnew) and min[1] = t .
9: xold= xnew
10: until stopping criteria is met

```
<p align="center">
  <img src="https://raw.githubusercontent.com/tanishkasingh9/Line-Search-Algorithm/master/Images/exact.png"> 
  </p>
