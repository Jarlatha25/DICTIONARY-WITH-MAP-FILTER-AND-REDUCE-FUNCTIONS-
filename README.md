# DICTIONARY-WITH-MAP-FILTER-AND-REDUCE-FUNCTIONS-
from functools import reduce
employees = {
&quot;Ravi&quot;: 45000,
&quot;Anita&quot;: 72000,
&quot;Karthik&quot;: 52000,
&quot;Priya&quot;: 38000,
&quot;Suresh&quot;: 61000
}
# map → 10% salary hike
updated = dict(map(lambda x: (x[0], int(x[1]*1.1)), employees.items()))
# filter → salary ≥ 50000
eligible = dict(filter(lambda x: x[1] &gt;= 50000, updated.items()))
# reduce → total salary
total = reduce(lambda a, b: a + b, updated.values())
print(updated)
print(eligible)
print(&quot;Total Salary:&quot;, total)
def deposit(bal, amt):

return bal + amt
def withdraw(bal, amt):
return bal - amt if amt &lt;= bal else bal
acc_no = 1001
name = &quot;Suresh&quot;
balance = 25000
balance = deposit(balance, 5000)
balance = withdraw(balance, 3000)
print(acc_no, name, balance)
Output:
{&#39;Ravi&#39;: 49500, &#39;Anita&#39;: 79200, &#39;Karthik&#39;: 57200, &#39;Priya&#39;: 41800, &#39;Suresh&#39;: 67100}
{&#39;Anita&#39;: 79200, &#39;Karthik&#39;: 57200, &#39;Suresh&#39;: 67100}
Total Salary: 294800
1001 Suresh 27000
