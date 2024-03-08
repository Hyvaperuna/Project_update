---
title: "Project update: species range shift"
author: " Sissi Liu "
output: html_document
--- 

_Published: march 7, 2024_



### **Summary**

-------------

#### 1.1 Main updates since last meeting 

* We investigated what caused anomalous patterns in the previous results and concluded that the anomalies were driven by the terminal effects in the model.
* We eliminate the terminal effects by iterating an infinite game in a time-invariant environment. Previously, the terminal payoffs were based on some arbitrary scrap values.
* Improved code and the model can be run more efficienctly.
* Article is NOT yet updated, the overleaf link: https://www.overleaf.com/read/rxspbgpynqkt#c11598

#### 1.2 Key assumptions about the model: Fixed quota share (FQS) 

* Catch quota ($\sigma$) follows the quota agreement that is optimal under pre-climate change conditions (i.e., no range shift, $k=0$) and the quota share is **fixed** in the post-climate change conditions ($k>0$).
* $\sigma$ is assumed equal to initial stock ownership: i.e., $\sigma=\theta_0$. 
* Previously $\sigma^* \geq \theta_0$, and we allow $\sigma^* > \theta_0$ in order to guarantee a cooperation solution for all $\theta_0$ and $k$. This implies that cooperation may not be possible if **assymetry in stock ownership becomes too large**. 
 

### **Update on main results** 

-----------


#### 2.1 Fixed quota shares (FQS) + side-payment (part of the quotas can be harvested in the other's waters) 

* With side-payment, the greatest losses occur when:
  +  the stock-losing country is the major owner, and
  +  the speed of range shift ($k$) is moderately fast.

<img src="C:/Users/a34543/Documents/vigo/mikko-repo/results/Sidepayment_rep200_04mar24.jpeg" alt="image2" width="550"/> 


####  2.2 FQS but without side payment (all fish quotas are harvested in their own waters)
														
The greatest losses happen if:

* the stock-losing country is the minor owner 
* the speed of range shift ($k$) is moderately fast.

<img src="C:/Users/a34543/Documents/vigo/mikko-repo/results/noSidepayment_rep200_mar062024.jpeg" alt="image2" width="550"/> 

#### 2.3 The effect of side payment 

We evaluate the effect of side-payment by subtracting the corresponding bio-economic values for scenario 1 from those in scenario 2. Results show clearly that side-payment changes harvest incentives.

* Side payment prevents a stock-losing country from defecting (the purple area in the figure below) if she were a minor owner (e.g., $\theta_0 \approx 0.25$). 
* Side payment increases the incentive of a stock-losing country to over-exploit the stock (the yellow area) if she were a major owner (e.g., $\theta_0 \approx 0.7$). 
* These results may have an important policy implication.
	
<img src="C:/Users/a34543/Documents/vigo/mikko-repo/results/Diff_Sidepayment_rep200_mar062024.jpeg" alt="image2" width="550"/>



### **Shift of game strategy with $\theta_0$ (x-axis) and $k$ (y-axis)** 

---------------
NOTE:

a. **Blue** denotes the areas where a stock-losing country (\#1) wants to defect
b. **Yellow** denotes the areas where a stock-receiving country (\#2) wants to defect 
c. **Grey** denotes both countries are willing to cooperate.
d. **White & black lines** indicate game strategies and the distribution of stock trajectories in a forward realization.

#### 3.1 Game strategies and stock trajectories WITH side-payment
* $x$ axis =$\theta_0$, $y$ axis=speed of range shift ($k$)

<img src="C:/Users/a34543/Documents/vigo/mikko-repo/results/P2strategyplots.png" alt="image2" width="600"/>


#### 3.2 Game strategies and stock trajectories WITHOUT side-payment
* $x=\theta_0$, $y=$speed of range shift ($k$)


<img src="C:/Users/a34543/Documents/vigo/mikko-repo/results/P2strategyplotnosidepay.png" alt="image2" width="600"/>

#### 3.3 Optimal harvest strategies with side-payment 
NOTE:

a. **h1, h2** refer to harvest strategies for stock-losing country and stock-receiving country, respectively.
b. **stk** refers to the stock trajectory.
c. dotted **coop** indicates countries are in cooperation ($1$-coop, $0=$ nash)
d. dashed **green** line indicate when $\theta=0.5$, i.e., countries have equal shares. 

<img src="C:/Users/a34543/Documents/vigo/mikko-repo/results/dignostics/policy_stockDynamics2.jpg" alt="image3" width="500"/>

Harvest dynamics result from interplays of the following factors:

* Free-ride incentive: minor owner has more incentive to over-harvest the stock
* Fixed-quota share (FQS): favours the stock-losing country, reduces her incentive to defect.
* FQS + side-payment: side-payment reduces the incentive of stock-receiving country to conserve the stock.


## To do list

* Update species distribution map for the empirical study part.
* Update literature from the last 3 years. 



