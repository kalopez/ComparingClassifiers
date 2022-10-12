notebook link:

This application uses a dataset from the UCI Machine Learning Repository 
which contains data from a Portuguese banking institution. It is a 
collection of the results of 17 marketing campaigns that occurred between 
May 2008 and November 2010.

Input variables:

1 - age
2 - job : type of job 
3 - marital : marital status
4 - education
5 - default: has credit in default?
6 - housing: has housing loan?
7 - loan: has personal loan?
8 - contact: contact communication type
9 - month: last contact month of year
10 - day_of_week:
11 - duration: last contact duration, in seconds (numeric). 
12 - campaign: number of contacts performed during this campaign and for 
this client
13 - pdays: number of days that passed by after the client was last 
contacted from a previous campaign (numeric; 999 means client was not 
previously contacted)
14 - previous: number of contacts performed before this campaign and for 
this client
15 - poutcome: outcome of the previous marketing campaign
16 - emp.var.rate: employment variation rate - quarterly indicator 
17 - cons.price.idx: consumer price index - monthly indicator
18 - cons.conf.idx: consumer confidence index - monthly indicator 
19 - euribor3m: euribor 3 month rate - daily indicator
20 - nr.employed: number of employees - quarterly indicator

Output variable (desired target):
21 - y - has the client subscribed a term deposit? (binary: 'yes','no')

Findings:
Using the correlation matrix and the partial_dependence function, the following features seem to best predict outcome:

1. nr.employed - Number of employees employed showed a negative correlation, those with smaller number of employees are more likely to subscribe.
2. duration - Call durations has a positive correlation, with higher call durations more likely to result in a subscription.
3. pdays - Number of days passed from last contact. Less days show better results. 
4. previous - number of contacts before this campaign for this client. More contacts show better results.
5. age - Age shows a slight positive correlation to likelihood of subscribing, with older individuals more likely to subscribe.

Recommendations:
1. Since duration is not known before a call is performed and cannot be as easily manipulated, it is included only for information purposes.
2. Decrease elapsed number of days for contacting clients in-between campaigns.
3. Increase number of contacts before campaigns for each client.
4. Clientele with less number of employees are the most likely to subscribe.

