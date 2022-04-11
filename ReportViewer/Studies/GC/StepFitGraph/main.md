# Step Fit Graph

If enabled the djuli calibrates a fit for the given concentrations. This fit generates the Step Fit Graph and the Step Fit Summary Table.

***Parameters:***

​		Fit formula: 

​				Linear: *y = ax + b*

​				Quadratic: *y = ax^2 + bx +c*

​				Inverse square root: *y = ax^0.5 + b*

​				Semilog x: *y = a log10(x) +b*

​				Semilog y: *log(y) = ax +b*

​				Double log: *log(y) = a log10(x) +b*

​				Exponential x: *y = a exp(x) +b*

​				Exponential y: *exp(y) = a exp(x) +b*

​				Michaelis-Menten: *1/y = a/x +b*

​		

![](StepFitGraph.png)

A. **Legends:** Defines the color-coded identifier of the confidence, calibrated and original values.

B. **Y-axis:** Magnitude of current. The units can be modified in 'Properties -> General -> Units -> Current (output)'

C. **X-axis:** Concentration. The untis can be changed in 'Properties -> General -> Units -> Units'

D. **Graph equation:** equation of the fitted line on the concentrations
