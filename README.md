# Homework Assignment 12


**Note**: Feel free to use any part of code from the 
[solution](https://github.com/HPM573/HW_5_Solution) 
to [Homework Assignment 5](https://github.com/HPM573/HW_05).


**Overview**. We'd like to use the continuous-time Markov Model of Atrial fibrillation we developed in 
HW 5 to evaluate 
the performance of anticoagulation using cost-utility and cost-benefit methods.

**Problem 1: Discounted Cost and Utility (Weight 1)**. Report the average discounted cost and QALY of 
patients who start in start "Well" under both scenarios of with and without anticoagulation: 
- Use the discount rate 3%.
- Assume that the utility of being in state “Well” is 1, 
in state “Stroke” is 0.2, and in state “Post-Stroke” is 0.9.
- The annual cost of being in “Post-Stroke” is $200 and when anticoagulation is used, this cost increases to $2000.
- Stoke results in a one-time cost of $5,000. 

**Problem 2: Change in Outcomes (Weight 1)**. 
Estimate the change in the expected discounted cost, the expected discounted utility, 
and the expected number of strokes when the anticoagulation drug is used. 
Report the 95% confidence intervals for all your estimates. 

*Note:* To find the present value of an outcome (say, $1000) 
that occurs at a certain point in time (say, $t$), discounted continuously, 
you can use the function `pv_single_payment`:

```python
import deampy.econ_eval as econ

present_value = econ.pv_single_payment(
    payment=1000,
    discount_rate=0.03,
    discount_period=t,
    discount_continuously=True)
```

**Problem 3: Cost-Utility Analysis (Weight 1)**. Use a cost-utility plane to display 
the expected discounted incremental utility and cost form the anticoagulation drug. 
Report the results of your cost-utility analysis in a table. 
Make sure to include the 95% confidence intervals for all reported estimates 
(discounted cost, discounted utility, incremental discounted cost, 
incremental discounted utility and the ICER).   

**Problem 4: Cost-Benefit Analysis (Weight 1)**. 
Plot the incremental net monetary benefit curve when the anticoagulation drugs 
is used for varying values of willingness-to-pay. 
Show the 95% confidence region. 
At what level of willingness-to-pay would you recommend adopting this 
anticoagulation drug?  
