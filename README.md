# Analysis-of-Active-B-Complaint-Backlog

Objective: Develop a strategy to address B complaint backlog, while maintaining adequate service level on new B complaints – making a best effort to stay below or near the CPR target of 40 days (average) to respond. 

#Data
Total of 11887 open B complaints, average of 89.8 workdays open, oldest complaint is 306.7 workdays.


#Methods
The first step was to redistribute total universe of b complaints into a smaller number of operational buckets. Needed strike a balance between total volume and mean workdays of each bucket while keeping a reasonable number of total buckets to simplify as an operational tool. Assumptions based on annual averages - approximately 5K new B complaints each month, approximately 5K B complaints inspected each month. Purpose was to meet objective of targeting/addressing backlog while maintaining adequate service level. 



Linear programming determined best method to optimize results. LP can be used because with increased number of inspectors, the average time to respond decreses linearly.

The first step in linear programming modelling is to devise an equation that is to be optimized. For this anslysis, this equation was used:

ART = M1*


#Results
