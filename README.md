# Minimizing-Economic-Cost-of-Power-Systems
**Minimizing Economic Cost for Power Systems with  Distinct Startup Times and Costs

*Abstract*: There many forms of power plant types in many different configurations that can be implemented in 
grid design. This paper is meant to show an optimization method for steam, combined cycle and gas 
turbines to meet the system demands of the ISO (Independent System Operator). Here, the amount the 
minimum and maximum a unit can produce, cost of fuel, grid demand, and distinct hot, warm, and cold 
start-up times and cost will be considered. In order to highlight the methods associated with the distinct 
hot, warm, cold start-up times the network grid losses, and impedance of the system will be neglected. 

Abstract: 
    There many forms of power plant types in many different configurations that can be implemented in 
grid design.  This paper is meant to show an optimization method for steam, combined cycle and gas 
turbines to meet the system demands of the ISO (Independent System Operator).   Here, the amount the 
minimum and maximum a unit can produce, cost of fuel, grid demand, and distinct hot, warm, and cold 
start-up times and cost will be considered.  In order to highlight the methods associated with the distinct 
hot, warm, cold start-up times the network grid losses, and impedance of the system will be neglected.   
Introduction: 
     The characteristic equation to consider in this type of optimization problem is to minimize the total cost 
of fuel supply.   Every turbine has a particular quadratic characteristic input-output characteristic equation 
for its incremental fuel rate [1]. 
�
�𝑓𝑖(𝑃𝐺𝑖)=𝑎𝑖𝑃𝐺𝑖
 2+𝑏𝑖𝑃𝐺𝑖+𝑐𝑖                            1 
where 𝐶𝑓𝑖 is the cost of fuel/hr input into the system, 𝑃𝐺𝑖 is the power being produced by a the turbine and 
�
�𝜖[1,2…𝑛] where 𝑛 is the number of turbines, and𝑎𝑖,𝑏𝑖,𝑎𝑛𝑑 𝑐𝑖 are constants associated with the 𝑖𝑡ℎ  
turbine.  Here the performance measure to be solved is formed: 
�
�𝑖𝑛𝐶𝑓𝑖(𝑃𝐺𝑖)=∑ 𝐶𝑓𝑖(𝑃𝐺𝑖) 𝑛
 𝑖=1                                                               2                                                
     Here, constraints on the turbines should also be considered: 
∑ 𝑃𝐺𝑖=𝑃𝐷 𝑛
 𝑖=1                                                                          3 
�
�𝐺𝑖𝑚𝑖𝑛≤𝑃𝐺𝑖≤𝑃𝐺𝑖𝑚𝑎𝑥                                                                  4 
 where 𝑃𝐺𝑖𝑚𝑖𝑛 , and 𝑃𝐺𝑖𝑚𝑎𝑥
 are the generators minimum and maximum production capacity respectively, 
and 𝑃𝐷 is the amount of power dispatched (power demanded from the plant by the ISO). 
Methods: 
 The Lagrange augmented function using constraint (3) and the Lagrange multiplier, 𝜆, can be rewritten 
from constraint (3) as: 
�
�(𝑃𝐺𝑖,𝜆𝑖)= 𝐶𝑓𝑖(𝑃𝐺𝑖)−𝜆(∑ 𝑃𝐺𝑖−𝑃𝐷 𝑛
 𝑖=1 )                                                           . 
Thus, in order to find 𝜆𝑖, set  𝜕𝐿(𝑃𝐺𝑖,𝜆𝑖)
 𝜕𝑃𝐺𝑖
 = 0 . Thus,  
                                    𝜕𝐿(𝑃𝐺𝑖,𝜆𝑖)
 𝜕𝑃𝐺𝑖
 =𝜕(𝐶𝑓(𝑷))
 𝜕𝑃𝐺𝑖
 −𝜆 𝜕
 𝜕𝑃𝐺𝑖
 (∑ 𝑃𝐺𝑖−𝑃𝐷 𝑛
 𝑖=1 )=0                                                 .  
Here, 𝜕
 𝜕𝑃𝐺𝑖
 (∑ 𝑃𝐺𝑖−𝑃𝐷 𝑛
 𝑖=1 )=𝜕𝑃𝐺𝑖
 𝜕𝑃𝐺𝑖
 =1. Thus, 𝜕(𝐶𝑓(𝑷))
 𝜕𝑃𝐺𝑖
 −𝜆=0.  It follows that, 
�
� =𝜕(𝐶𝑓(𝑷))
 =𝜕(𝐶𝑓(𝑷))
 =⋯=𝜕(𝐶𝑓(𝑷))
 𝜕𝑃1
 𝜕𝑃2
 𝜕𝑃𝑛
 This is derived in previous work as the principle of equal incremental rate [2].  
Taking the partial derivatives of equation (1) as disrobed in equation (5) we obtain: 
�
� =𝑎1𝑃𝐺1 +𝑏1 = 𝑎2𝑃𝐺2 +𝑏2 = ⋯ = 𝑎𝑛𝑃𝐺𝑛 +𝑏𝑛                                             
We can rewrite equation (6) into n-1 equations.  This system of equations combined with the original 
constraint equation will allow for the solving of optimization of the system neglecting the min/max 
constraint of the generator.  This gives a global optimum without the constraints considered. 
5  
6                 
There are several ways to approach to accounting for the constraints in the optimization search: Using 
General Constraints with Lagrange Multipliers, Using Outside Penalty Function, etc.   However, none 
seem as intuitively obvious as maximizing or minimizing the 𝑃𝐺𝑖 variable that violated the constraint 
followed by adjusting the 𝑃𝐷 to equate for the difference in demand.    
Assume 𝑃𝑗 violated constraint (4) where 𝑗𝜖[1,2…𝑛].  Thus, the global maximum is outside the 
constraint and we let 𝑃𝑗𝑛𝑒𝑤 = 𝑃𝑗𝑚𝑎𝑥/𝑚𝑖𝑛 closest to optimization point.  Letting ∆𝑃 =  𝑃𝑗 − 𝑃𝑚𝑖𝑛/𝑚𝑎𝑥 we have 
�
�𝐷𝑛𝑒𝑤 = 𝑃𝐷 −∆𝑃.  Following this procedure equations (3), and (6) to obtain the optimum excluding 𝑃𝑗 from 
the calculations to obtain the optimum can be used a second time.    
The startup costs associated with dispatching a turbine needs to also be considered.  The cooler a 
turbine is the longer it will take to come on line and the more fuel will be used in the process.   This can 
be modeled as such: 
�
�𝑠𝑓(𝑡) = 𝐹(1−𝑒−𝑡 𝜏 ⁄) +𝐶𝑚                                                               
7 
where 𝐶𝑠𝑓(𝑡) is the total cost of startup fuel, 𝐹 is the cost fuel, t is the time the unit has been offline,𝜏 is the 
thermal time constant derived from the cool down time of the unit, and 𝐶𝑚 is the cost of the maintenance 
of the start-up [4].   This does not address the nature of the discreteness of start-up procedures for three 
distinct different states: hot start, cold start, and warm start  The steam or combined cycle turbines start
up time and procedure is said to be in the hot, warm, or cold start up state if 𝑡𝜖[𝑡ℎ𝑜𝑡 𝑚𝑖𝑛,∞], 
�
�𝜖[𝑡𝑤𝑎𝑟𝑚 𝑚𝑖𝑛,𝑡ℎ𝑜𝑡 𝑚𝑖𝑛], or 𝑡𝜖[𝑎𝑚𝑏𝑖𝑎𝑛𝑡 𝑡𝑒𝑚𝑝𝑒𝑟𝑎𝑡𝑢𝑟𝑒,𝑡𝑤𝑎𝑟𝑚 𝑚𝑖𝑛] respectively*.  This means that for every 
turbine the hot start cost, 𝐶𝐺𝑖ℎ, Warm start,  𝐶𝐺𝑖𝑤, and cold start costs, 𝐶𝐺𝑖𝑐,constant values for 𝑖 number 
turbine exists.  These constants can be calculated from equation 1 knowing 𝐹, 𝐶𝑚,𝑡,𝑎𝑛𝑑 𝜏.  Thus, 
�
�𝑠𝑓𝐺𝑖(𝑡) = {
 𝐶𝐺𝑖𝑐 𝑤ℎ𝑒𝑟𝑒       𝑡𝜖[𝑎𝑚𝑏𝑖𝑎𝑛𝑡 𝑡𝑒𝑚𝑝𝑒𝑟𝑎𝑡𝑢𝑟𝑒,𝑡𝑤𝑎𝑟𝑚 𝑚𝑖𝑛] 
�
�𝐺𝑖𝑤 𝑤ℎ𝑒𝑟𝑒                                   
�
�𝜖[𝑡𝑤𝑎𝑟𝑚 𝑚𝑖𝑛,𝑡ℎ𝑜𝑡 𝑚𝑖𝑛] 
�
�𝐺𝑖ℎ
 𝑤ℎ𝑒𝑟𝑒                                                  
where 𝐶𝑠𝑓𝐺𝑖(𝑡) is the start-up cost for turbine 𝑖. 
�
�𝜖[𝑡ℎ𝑜𝑡 𝑚𝑖𝑛, ∞]
 }                         
It should be noted here that there are the hot, warm, and cold start-up procedures for the steam and 
combined cycle but not GTs.  The GTs are made for quick dispatch and can be readily available to run 
when called.  It is for this reason 𝐶𝑠𝑓𝐺𝑖(𝑡) = 0 for GTs. 
8 
Other constraints not considered such as network losses, maintenance being performed on the 
system, and transformer losses.   Many of these add the nodal currents, voltages, transformer taps, 
season, and many others variables to the picture for optimization of the power grid.   All of these variables 
go into a Smart-Grid system with further complexity.  This paper is focused only on the implementation of 
the discrete costs associated with Hot, Warm, and Cold start-up procedures.    
Example of Generator Configuration for a modern Power Plant: 
Let the power demand for the next 7 hours be displayed as follows in Table 1:  
Suppose the plant under question has 3 Gas Turbines (GTs) where 10𝑀𝑊 ≤ 𝑃𝐺𝑇1 ≤ 20𝑀𝑊,
 15𝑀𝑊 ≤𝑃𝐺𝑇2 ≤30𝑀𝑊,𝑎𝑛𝑑  13𝑀𝑊 ≤𝑃𝐺𝑇3 ≤25𝑀𝑊. The plant also contains one steam turbine 
generator (ST)  where 50𝑀𝑊 ≤ 𝑃𝑆𝑇1 ≤ 522𝑀𝑊, and one combined cycle (CC) plant where 10𝑀𝑊 ≤
 𝑃𝐶𝐶1 ≤ 300𝑀𝑊. The GTs, ST, and CC  have a charicterized function for the cost as follows: 
�
�𝑆𝑇1(𝑃𝑆𝑇1) = .0082𝑃𝑆𝑇1
 2 + 18.67𝑃𝑆𝑇1 − 500   
�
�𝐶𝐶1(𝑃𝐶𝐶1) = −.0521𝑃𝐶𝐶1
 2 + 41.403𝑃𝐶𝐶1 + 1848
 𝐶𝐺𝑇1(𝑃𝐺𝑇1) = −1.5𝑃𝐺𝑇1
 2 + 163𝑃𝐺𝑇1 + 429.76
 𝐶𝐺𝑇2(𝑃𝐺𝑇2) = −2.66𝑃𝐺𝑇2
 2 + 184𝑃𝐺𝑇2 +390   
�
�𝐺𝑇3(𝑃𝐺𝑇3) = −1𝑃𝐺𝑇3
 2 + 125𝑃𝐺𝑇3 + 809         
With the current price of gas $4.48 MCF, the associated costs of different start-up procedures for the  
cold, warm, and hot starts of the ST and CC and times are as follows in Table 2: 
The ST has been offline for 2 hours, while the CC turbine has been off line for 4 hours. 
It is assumed in this problem that all turbines are starting from the off position with an entire plant 
outage taking place.  Also, all GTs are assumed to have a 0hr start-up time. 
For the first two hours the only available turbines will be the GTs.  This is due to the start-up times of 
the ST and CC turbines. In this problem the ST can be available 3 hours from now and the CC turbine 2 
hours from now.  We consider the following availability of the turbines in Table 3 
We can use equation (6) as previously derived to form the Lagrange multiplier.  Thus,  
�
�𝐶𝐺𝑇1(𝑃𝐺𝑇1)
 𝜕𝑃𝐺𝑇1
 𝜕𝐶𝐺𝑇2(𝑃𝐺𝑇2)
 𝜕𝑃𝐺𝑇2
 =−3𝑃𝐺𝑇1 +163
 =−5.32𝑃𝐺𝑇2 +184
 𝜕𝐶𝐺𝑇3(𝑃𝐺𝑇3)
 𝜕𝑃𝐺𝑇3
 =−1𝑃𝐺𝑇3 +125
 𝜕𝐶𝑆𝑇1(𝑃𝑆𝑇1)
 𝜕𝑃𝑆𝑇1
 =.0164𝑃𝑆𝑇1 +18.67
 =−.1042𝑃𝐶𝐶1 +41.403  
�
�𝐶𝐶𝐶1(𝑃𝐶𝐶1)
 𝜕𝑃𝐶𝐶1
 As derived from the Lagrange multiplier (6) we can consider the system of equations: 
−3𝑃𝐺𝑇1 +163 = −5.32𝑃𝐺𝑇2 +184 = −1𝑃𝐺𝑇3 +125 ⟹
 −3𝑃𝐺𝑇1 +5.32𝑃𝐺𝑇2 = 21
 −5.32𝑃𝐺𝑇2 + 1𝑃𝐺𝑇3 = −59                                        
Table 1 can be seen as an hourly constraint similar to equation (3).  Demanded at start (h=0) is 40 MW.  
Thus, 
�
�𝐺𝑇1 + 𝑃𝐺𝑇2 +𝑃𝐺𝑇3 = 40                                                       
Equations (9) and (10) can be solved as a system with the result: 
�
�𝐺𝑇1 = 16.17𝑀𝑊,𝑃𝐺𝑇2 = 13.29𝑀𝑊,𝑃𝐺𝑇3 = 10.52𝑀𝑊   
The result in (11) can be seen as the global minimum.  We can see that 𝑃𝐺𝑇2 and 𝑃𝐺𝑇3 have both 
violated the constraint by being too low.   This means that  𝑃𝐺𝑇2, and 𝑃𝐺𝑇3 will be increased to their 
minimum points and the maximum power recalculated.  Thus, 𝑃𝐺𝑇2 = 15𝑀𝑊, and 𝑃𝐺𝑇3 = 13𝑀𝑊.   This 
results in 𝑃𝐺𝑇1 = 12𝑀𝑊 to meet the demand at h=0.   
9 
10 
For 1 hour in the future, equations (9) and (10) are repeated only the constraint in equation (10) is 60.  
This results in: 
�
�𝐺𝑇1 = 20.54𝑀𝑊,𝑃𝐺𝑇2 = 15.80𝑀𝑊,𝑃𝐺𝑇3 = 23.64𝑀𝑊   
We see here 𝑃𝐺𝑇1 has violated the constraint.   Thus, we reduce 𝑃𝐺𝑇1 to 20MW and add the difference to 
be made up by the minimum between 𝑃𝐺𝑇2 and 𝑃𝐺𝑇3.   Here we change the demand to 40MW.   Thus, we 
solve the system of equations created by: 
−5.32𝑃𝐺𝑇2 + 184 = −1𝑃𝐺𝑇3 +125 and 𝑃𝐺𝑇2 +𝑃𝐺𝑇3 = 40 
This system solved: 
�
�𝐺𝑇2 = 15.89𝑀𝑊,𝑃𝐺𝑇3 = 24.1𝑀𝑊   
Thus, after the first hour the optimal configuration is  
�
�𝐺𝑇1 = 20𝑀𝑊,𝑃𝐺𝑇2 = 15.89𝑀𝑊,𝑃𝐺𝑇3 = 24.1𝑀𝑊   
Two hours from the start we must now consider the combined cycle turbine since it can go online 
within two hours.  Here, the cost of start-up is different constants,  𝐶𝐶𝐶𝐶𝑜𝑙𝑑,  and  𝐶𝐶𝐶𝐻𝑜𝑡 start-ups.  As a 
result the partial derivatives used in (6) do not reflect these costs.   It must be added to the optimum and 
the choice to start or not to start the turbine must be determined.    
Considering two hours from now with only the GTs available we see  
�
�𝐺𝑇1 = 20𝑀𝑊,𝑃𝐺𝑇2 = 30𝑀𝑊,𝑃𝐺𝑇3 = 25𝑀𝑊   
Checking the performance measure (2) we see: 
�
�
 𝑚𝑖𝑛𝐶𝑓𝑖(𝑃𝐺𝑖) = ∑𝐶𝑓𝑖(𝑃𝐺𝑖)
 𝑖=1
 =3089+3516+3309 = $9914 
Considering all GTs and CC turbine using equation (6) we obtain the following set of equations: 
−3𝑃𝐺𝑇1 +163 = −5.32𝑃𝐺𝑇2 +184 = −1𝑃𝐺𝑇3 +125 = −.1042𝑃𝐶𝐶1 +41.403 
With the CC turbine now being considered the optimal is still: 
�
�𝐺𝑇1 = 20𝑀𝑊,𝑃𝐺𝑇2 = 30𝑀𝑊,𝑃𝐺𝑇3 = 25𝑀𝑊,𝑃𝐶𝐶1 = 0 𝑀𝑊  
This is due to the low level of efficiency of the CC turbine at lower MW production. 
For three hours from now the power being demanded is 300MW.  Here, the GTs alone cannot produce 
the load demanded and the CC turbine will need to be started up to fill the demand.   Using equality of the 
Lagrange multiplier and the system of equations method previously described: 
�
�𝐺𝑇1 = 45.0𝑀𝑊,𝑃𝐺𝑇2 = 29.32𝑀𝑊,𝑃𝐺𝑇3 = 97.0𝑀𝑊,𝑃𝐶𝐶1 = 128.66 𝑀𝑊 
Here, GT1 and GT3 are both in violation of the constraints and need to be maximized. Thus, 𝑃𝐺𝑇1 =
 20𝑀𝑊,𝑎𝑛𝑑  𝑃𝐺𝑇3 =25𝑀𝑊.   This leaves an optimization of 255MW for turbines 𝑃𝐺𝑇3 and 𝑃𝐶𝐶1.  Here, 
�
�𝐺𝑇1 = 20𝑀𝑊,𝑃𝐺𝑇2 = 99.7𝑀𝑊,𝑃𝐺𝑇3 = 25𝑀𝑊,𝑃𝐶𝐶1 = 155.2𝑀𝑊 
�
�𝐺𝑇2 violates the constraint and needs to be maximizes to 30MW.  This leaves 𝑃𝐶𝐶1 = 225𝑀𝑊 to make up 
the power demand constraint. This causes the total cost to be    
�
�
 ∑𝐶3𝑖(𝑃𝐺𝑖)
 𝑖=1
 +𝐶𝐶𝐶𝐶𝑜𝑙𝑑 = 16317 +6000 = 22,317 
We must consider the case of a warm-start up on the ST (Note: a cold start on CC and a warm-start 
on the ST both is not considered because of the start-up cost being great enough to exceeding the two 
situations of the CC start-up or the ST warm start-up.  Using previous methods: 
�
�𝐺𝑇1 = 47.5𝑀𝑊,𝑃𝐺𝑇2 = 30.7𝑀𝑊,𝑃𝐺𝑇3 = 104.4𝑀𝑊,𝑃𝑆𝑇1 = 117.4 𝑀𝑊 
Modified with this leaves 𝑃𝑆𝑇1 = 225𝑀𝑊.  This causes the total cost to be    
�
�
 ∑𝐶3𝑖(𝑃𝐺𝑖)
 𝑖=1
 +𝑪𝑪𝑪𝑪𝒐𝒍𝒅 = 16092+8000 = 24,092 
Thus, the optimal start-up for 3 hours from now is: 
�
�𝐺𝑇1 = 20𝑀𝑊,𝑃𝐺𝑇2 = 30𝑀𝑊,𝑃𝐺𝑇3 = 25𝑀𝑊,𝑃𝐶𝐶1 = 225 𝑀𝑊 
For 4 hours from now we have the CC running and it is now cheaper to run the CC because of start-up 
costs.  Thus, in order to meet demand: 
�
�𝐺𝑇1 = 20𝑀𝑊,𝑃𝐺𝑇2 = 30𝑀𝑊,𝑃𝐺𝑇3 = 25𝑀𝑊,𝑃𝐶𝐶1 = 300 𝑀𝑊 
For hour 5 the Steam Turbine must be run to meet the demand of 600MW.   However, the turbine can 
only be used in a cold start since it has been offline for more than 4 hours.  Using the Lagrange multiplier 
technique previously described: 
�
�𝐺𝑇1 = 47.63𝑀𝑊,𝑃𝐺𝑇2 = 30.80𝑀𝑊,𝑃𝐺𝑇3 = 104.89𝑀𝑊,,𝑃𝑆𝑇1 = 87.25 𝑀𝑊,𝑃𝐶𝐶1 = 204.4 𝑀𝑊  
Here, all GTs have violated the maximum constraint and 𝑃𝐺𝑇1 = 20𝑀𝑊,𝑃𝐺𝑇2 = 30𝑀𝑊,𝑃𝐺𝑇3 = 25𝑀𝑊 
where the CC and ST turbines have to make up the difference.   With this consideration the new power 
demand for the ST and CC is 400MW.  Using this as the demand between the two: 
�
�𝐺𝑇1 = 20𝑀𝑊,𝑃𝐺𝑇2 = 30𝑀𝑊,𝑃𝐺𝑇3 = 25𝑀𝑊,𝑃𝑆𝑇1 = 215.83 𝑀𝑊,𝑃𝐶𝐶1 = 184.16𝑀𝑊 
Starting the ST adds significantly to the cost which we will see later. 
Finally, for 6 hours from now evaluated using previous methods we have: 
�
�𝐺𝑇1 = 20𝑀𝑊,𝑃𝐺𝑇2 = 30𝑀𝑊,𝑃𝐺𝑇3 = 25𝑀𝑊,𝑃𝑆𝑇1 = 67.48 𝑀𝑊,𝑃𝐶𝐶1 = 207.51𝑀𝑊 
It should be noted that shutting off a turbine once it is started up is not advised.   The cost of starting a 
turbine is significant and can severely increase the operational cost.  We see the hourly operational costs 
and power in table 4 
It can be seen that the profit is negative for the 1 hour and 2 hour.   This means it would be more 
profitable to not run the GTs.  However, the plant could be under capacity payments and ordered to run 
by the ISO with a compensation plan worked out for the distribution system.     
Conclusion: 
The method described here can be summed up in the following steps: 
1. Use the equality of the Lagrange multipliers to find a system of equations for the equality of the 
partial derivatives of the fuel characteristic equations, and the power demand formula.  Do this on 
only available units. 
2. Check if any units violated the constraint.  Maximize or minimize these units based on which way 
(greater than/less than) they violated the constraint. 
3. Disperse the power over the other units that did not violate the constraint and repeat step 1 to 
calculate the optimized power units left over. 
4. If there is cold, warm, or hot starts to consider take them as separate scenarios of each starting 
up and calculate total costs including start-up costs. 
5. Take the minimized cost as the optimum scenario. 
This is a feasible method to which an algorithm can be written for and incorporated in grid 
technologies.   Much of the work using the principle of equal incremental rate proved by equal 
Lagrange multipliers has been previously done, with the addition of the start-up cost assessment in 
this paper.   Different weightings to equation (5) can be further added to compensate for network 
losses[].   However, it is necessary to know the nodal current and voltages here.  
