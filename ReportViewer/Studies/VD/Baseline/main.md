# Baseline

If enabled, a baseline is applied to the Raw Data before the analysis. 

It substracts the function selected in Fit Baseline.

​				y* = y - f(x) 

​	where:

​			 y* := output value.

​			 y := original y value

​			x := original x value

​			f(x) :=  fitted function selected in the parameter Fit Baseline

***Parameters:***

​		**Fit Baseline:** 

​				Offset: f(x) = minimum(X)    i.e. minimum of all X values

​				Linear: *f(x) = ax + b*

​				Quadratic: *f(x) = ax^2 + bx +c*

​				Inverse square root: *f(x) = ax^0.5 + b*

​				Semilog x: *f(x) = a log10(x) +b*

​				Semilog y: *log(f(x)) = ax +b*

​				Double log: *log(f(x)) = a log10(x) +b*

​				Exponential x: *f(x) = a exp(x) +b*

​				Exponential y: *exp(f(x)) = a exp(x) +b*

​				Michaelis-Menten: *1/f(x) = a/x +b*

​		**Range Baseline:** defines the range where the baseline function is fitted.

​		