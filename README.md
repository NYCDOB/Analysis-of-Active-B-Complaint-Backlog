# Analysis-of-Active-B-Complaint-Backlog

Objective: Develop a strategy to address B complaint backlog, while maintaining adequate service level on new B complaints – making a best effort to stay below or near the CPR target of 40 days (average) to respond. 

#Data
Total of 11887 open B complaints, average of 89.8 workdays open, oldest complaint is 306.7 workdays.


#Methods
The first step was to redistribute total universe of b complaints into a smaller number of operational buckets. Needed strike a balance between total volume and mean workdays of each bucket while keeping a reasonable number of total buckets to simplify as an operational tool. Assumptions based on annual averages - approximately 5K new B complaints each month, approximately 5K B complaints inspected each month. Ran multiple scenarios to optimize – meet objective of targeting/addressing backlog while maintaining adequate service level. 


Linear programming was determined to be best method to optimize results. LP can be used because with increased number of inspectors, the average time to respond decreses linearly.

The first step in linear programming modelling is to devise an equation that is to be optimized. For this anslysis, here is the equation used:

ART = M1 * R1 + M2 * R2 + M3 * R3 + M4 * R4 + M5 * R5 + M6 * R6

Where ART is the average response time, M is the mean age of complaint for each category [0 to 40 days, 40 to 100, 100 to 150, 150 to 200, 200 to 250, 250 to 310], and R is the number of inspectors to be assigned to each category. 

For one of the scenarios, a constraint of 80% of the inspectors were placed on the first category [0 to 40 days] and 20% on the last category [250 to 310 days]. An additional constraint of a maximum of 40 days was also placed on the equation. The reason is that the city has a target of inspecting B complaints within 40 days, and the age of the oldest complaints could not be allowed to grow indefinately. 

#Results

	Buckets	Freq	Mean	Pct from each bucket	# of Proposed Responses	Responses * Mean	Avg Time to Respond
1	(0,40]	4102	13.8	78.01%	3200	44160	39.991074
2	(40,100]	2954	70.52	54.94%	1623	114453.96	
3	(100,150]	1875	122.31	0.00%	0	0	
4	(150,200]	1540	174.73	0.00%	0	0	
5	(200,250]	1074	223.49	12.01%	129	28830.21	
6	(250,310]	241	260.65	19.92%	48	12511.2	
Total		11786			5000	199955.37	




