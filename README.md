# Restaurant Tipping Behavior and Payment Patterns

## 1. Introduction / Motivation

This project explores tipping behavior in restaurants using the Seaborn `tips` dataset.

At first, I wanted to check the most intuitive relationship in the dataset: whether a higher total bill leads to a higher tip. However, while exploring the data, I became more interested in the behavioral patterns behind tipping rather than the tip amount alone.

As the analysis progressed, I began asking broader questions:

- Do tipping patterns differ by gender, day, or time?
- Is the variable `sex` better interpreted as the person who paid rather than everyone at the table?
- Could the dataset reflect social patterns such as couples dining together, especially during dinner?
- What additional data would be needed to make more accurate business decisions?

This project therefore developed from a simple bill-tip analysis into a behavioral interpretation of restaurant payment patterns.

---

## 2. Dataset

The analysis uses the Seaborn `tips` dataset, which contains information about restaurant bills and tips.

### Variables included in the dataset

- `total_bill`: total bill amount for the table
- `tip`: tip amount
- `sex`: sex of the bill payer
- `smoker`: whether the bill payer is a smoker
- `day`: day of the week
- `time`: lunch or dinner
- `size`: number of people at the table

In addition to the original variables, I created a derived variable:

- `tip_rate = tip / total_bill`

This variable was useful because tip amount alone can be misleading when total bill sizes differ across groups.

---

## 3. Exploratory Analysis

The analysis began by visualizing the relationship between `total_bill` and `tip` using a scatter plot. This showed a clear positive relationship, suggesting that tip amount tends to increase as the bill amount increases.

After that, I explored several other variables and relationships, including:

- tip amount by gender
- tip amount by day of the week
- tip rate by day of the week
- tip rate by smoker status
- boxplots of tip amount by day
- average tip by party size
- tip amount by party size
- number of tables by party size
- relationship between party size, total bill, and tip
- point distribution by smoker status
- boxplots of tip amount by lunch vs dinner
- boxplots of total bill by lunch vs dinner
- boxplots of tip amount by gender
- scatter distributions involving time, total bill, and payer sex
- boxplots of tip rate by gender
- average tip rate by day
- boxplots of tip rate by day

I also examined cross-tabulations such as:

- payer sex by table size
- payer sex by lunch vs dinner
- lunch vs dinner by table size

These visualizations were used not only to identify numerical relationships, but also to generate behavioral interpretations.

---

## 4. Key Findings

Several important patterns emerged from the analysis.

### 4.1 Positive relationship between total bill and tip
The scatter plot showed that higher total bills are generally associated with higher tips. This suggests a roughly linear positive relationship between bill amount and tip amount.

### 4.2 Tip amount and tip rate are not the same
While some groups appeared to leave larger tips in absolute terms, this did not always mean they had a higher `tip_rate`. Creating the `tip_rate` variable was important for comparing tipping behavior more fairly.

### 4.3 Dinner customers dominate the dataset
Dinner observations were much more common than lunch observations, suggesting that this restaurant may be more dinner-oriented.

### 4.4 Two-person tables are the most common
Tables of size 2 appeared much more frequently than other group sizes. This suggests that two-person dining is a major part of the restaurant’s customer base.

### 4.5 Male payers appear more often than female payers
Across the dataset, male payers appeared substantially more often than female payers. This difference became especially noticeable during dinner.

### 4.6 Lunch and dinner show different gender patterns
At lunch, male and female payer counts were relatively similar. At dinner, however, male payers appeared about 2.4 times more frequently than female payers.

### 4.7 Party size may affect tip rate
As party size increased, tip rate seemed to decrease somewhat. However, because the number of observations for larger parties was small, this pattern should be interpreted cautiously.

---

## 5. Behavioral Interpretation

The most interesting part of this analysis was not just identifying numerical patterns, but interpreting what they might mean behaviorally.

One important shift in interpretation occurred when I reconsidered the meaning of the variable `sex`. Rather than treating it simply as the gender of a customer at the table, it made more sense to interpret it as the sex of the person who paid the bill.

Once viewed this way, several patterns became more meaningful:

- male payers were more common overall
- two-person tables were dominant
- dinner showed a much higher proportion of male payers than lunch

This led to the hypothesis that the restaurant may receive many couple-based dinner visits, and that in those cases the male partner may more often pay the bill.

I also considered the possibility that when party size becomes larger, male payers may bear a greater financial burden because they are more often the payer for larger groups. This could help explain why male payers may show slightly lower tip rates despite paying larger bills.

These interpretations are not directly proven by the dataset, but they are plausible behavioral hypotheses generated through exploratory analysis.

---

## 6. Business Insights

The analysis suggests several possible business implications.

### 6.1 Couple-oriented promotions may be effective
Because dinner has a high proportion of male payers and two-person tables are especially common, the restaurant may benefit from targeting couples more directly.

Possible examples include:

- anniversary events
- couple dinner promotions
- romantic set menus
- celebration-based dining experiences

These kinds of events could potentially increase both customer satisfaction and tip-related outcomes.

### 6.2 Bill size may matter more than tip rate
From a business perspective, increasing total revenue may be more meaningful than focusing only on tip rate. Since tip amount tends to rise with total bill, strategies that increase bill size may be more effective overall.

Examples:

- dessert recommendations
- premium menu suggestions
- drink or wine upselling
- event-based packages

### 6.3 Table turnover-based analysis would be more useful for real revenue decisions
If the actual goal is to improve restaurant revenue, then total bill or tip per table alone may not be enough. A more realistic metric would be something like:

- total bill per table turnover
- tip per table turnover
- revenue per hour
- tip per hour

This would help connect tipping behavior to operational performance more directly.

---

## 7. Limitations & Further Data Needed

A major insight from this project is that the current dataset is useful, but incomplete.

Several important variables are not included, and without them it is difficult to make strong causal claims.

Additional variables that would improve the analysis include:

- server identity
- menu categories ordered
- whether the table consisted of a couple, family, or group of friends
- table duration / dining time
- special events such as anniversaries or celebrations
- customer age or demographic information

For example:

- if one server consistently receives higher tips, service quality may matter more than bill size alone
- if certain menu items are associated with larger tips, menu design could matter
- if couple tables tip differently from group tables, customer relationship context would be important
- if table turnover is slow, high bill amounts may not necessarily translate into better operational performance

In other words, the current dataset supports useful exploratory insights, but more complete behavioral and operational data would be necessary for stronger conclusions.

---

## 8. Conclusion

This project began as a simple attempt to examine the relationship between total bill and tip amount, but it developed into a broader exploration of tipping behavior and payment patterns.

The analysis showed that:

- total bill and tip are positively related
- dinner dominates the dataset
- two-person tables are especially common
- male payers appear more frequently, especially at dinner
- tip behavior may reflect broader social and payment patterns rather than bill size alone

Most importantly, this project highlighted that exploratory analysis is not only about finding patterns in graphs, but also about questioning the meaning of variables, generating behavioral hypotheses, and recognizing what additional data would be needed for more accurate conclusions.

This project therefore represents both a technical EDA exercise and a behavioral interpretation of restaurant payment data.
