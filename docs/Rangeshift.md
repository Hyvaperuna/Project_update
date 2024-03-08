---
title: "Project update: Species range shift"
author: " Sissi Liu "
output: html_document
--- 

_Published: march 8, 2024_



### 1 **Summary**

-------------

#### 1.1 Main updates since last meeting 

* We investigated what had caused anomalous patterns in the previous results and concluded that the anomalies were driven by the terminal effects in the model.
* We eliminate the terminal effects by iterating an infinite game in a time-invariant environment. Previously, the terminal payoffs were based on some arbitrary scrap values.
* Compared two scenarios: with and without side-payments
* Improved code and the model can be run more efficiently.


#### 1.2 Key assumptions about the model: Fixed quota share (FQS) 

* We model a **non-adaptive** fishery agreement by assuming catch quota $\sigma_t$ equal to initial stock ownership and is fixed over time: i.e., $\sigma_t=\theta_0$. This implies that cooperation may not be possible if **asymmetry in stock ownership becomes too extreme **.
  +  Previously, we assumed that $\sigma_t=\sigma^*$, where $\sigma^*=f(\theta_0|k=0)$, and $\sigma^*\geq\theta_0$   
* **Side-payment**: We model side-payments by assuming that a portion of the quota can be fished in the waters of the other country. 
* Single-owner optium is used as the reference case to evaluate losses under different scenarios.

### 2 **Update on main results** 

-----------


#### 2.1 Scenario 1: Fixed quota shares (FQS) + side-payments

With side-payment, the greatest losses occur when:

* the stock-losing country is the major owner, and
* the speed of range shift ($k$) is moderately fast.

<span style="color:blue;">
_NOTE: Legend text "Ratio" refers to the proportion of loss/gain relative to the sole-owner optium._
</span>

<img src="C:/Users/a34543/Documents/vigo/mikko-repo/results/Sidepayment_rep200_04mar24.jpeg" alt="image2" width="550"/> 


####  2.2 Scenario 2: FQS but without side payments
														
The greatest losses happen if:

* the stock-losing country is the minor owner 
* the speed of range shift ($k$) is moderately fast.

<img src="C:/Users/a34543/Documents/vigo/mikko-repo/results/noSidepayment_rep200_mar062024.jpeg" alt="image2" width="550"/> 

#### 2.3 The effect of side payments 

We evaluate the effect of side-payment by subtracting the corresponding bio-economic values for scenario 1 from those in scenario 2. The results clearly show that side-payments alter harvest incentives.

* Side payment prevents a stock-losing country from defecting (the purple area in the figure below) if she were a minor owner (e.g., $\theta_0 \approx 0.25$). 
* Side payment increases the incentive of a stock-losing country to over-exploit the stock (the yellow area) if she were a major owner (e.g., $\theta_0 \approx 0.7$). 
* These results may have an important policy implication.
	
<img src="C:/Users/a34543/Documents/vigo/mikko-repo/results/Diff_Sidepayment_rep200_mar062024.jpeg" alt="image2" width="550"/>



### 3 **Shift of game strategy with $\theta_0$ and $k$ ** 

---------------
NOTE:

a. **Blue** denotes the areas where a stock-losing country (\#1) wants to defect
b. **Yellow** denotes the areas where a stock-receiving country (\#2) wants to defect 
c. **Grey** denotes both countries are willing to cooperate.
d. **White & black lines** indicate game strategies and the distribution of stock trajectories in forward realizations.

#### 3.1 Game strategies and stock trajectories WITH side-payment
* $x$ axis =$\theta_0$, $y$ axis=speed of range shift ($k$)

<img src="C:/Users/a34543/Documents/vigo/mikko-repo/results/P2strategyplots.png" alt="image2" width="600"/>


#### 3.2 Game strategies and stock trajectories WITHOUT side-payment
* $x=\theta_0$, $y=$speed of range shift ($k$)


<img src="C:/Users/a34543/Documents/vigo/mikko-repo/results/P2strategyplotnosidepay.png" alt="image2" width="600"/>

#### 3.3 Optimal harvest strategies with side-payment 
NOTE:

a. **h1, h2** refer to harvest proportion ($1-p$) for stock-losing country and stock-receiving country, respectively.
b. **stk** refers to the stock trajectory.
c. dotted **coop** indicates countries are in cooperation ($1=$coop, $0=$ nash)
d. dashed **green** line indicate when $\theta=0.5$, i.e., countries have equal shares. 

<img src="C:/Users/a34543/Documents/vigo/mikko-repo/results/dignostics/policy_stockDynamics2.jpg" alt="image3" width="500"/>

Harvest dynamics result from interplays of the following factors:

* Free-ride incentive: minor owner has more incentive to over-harvest the stock
* Fixed-quota share (FQS): favours the stock-losing country, reduces her incentive to defect.
* FQS + side-payment: side-payment reduces the incentive of stock-receiving country to conserve the stock.


## To do list

* Update species distribution map for the empirical study part.
* Update literature from the last 3 years. 



