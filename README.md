This is an assignment for Berkley Engineering to understand the likelihood of drivers accepting coupons on the road (based off an Amazon database)

# Practical Application Assignment 5.1 (UC Berkeley AI/ML Prof Certification)
This file contains a summary of findings from exploration of a dataset from the UCI Machine Learning repository. The data was collected via a survey on Amazon Mechanical Turk. The purpose of the exploration was to determine characteristics of drivers who are more likely to accept coffee house coupons.

# Brief Description of the Dataset
The dataset is based on a survey describing different driving scenarios, including the destination, current time, weather, passenger, etc., and then asking people whether they will accept the coupon if they are the driver. Answers given that the users will drive there “right away” or “later before the coupon expires” are labeled as “Y = 1”, and answers “no, I do not want the coupon” are labeled as “Y = 0”. There are five different types of coupons—less expensive restaurants (under $20), coffee houses, carry out and take away, bars, and more expensive restaurants ($20–$50). The current work focuses on identifying attributes that provide a higher likelihood of drivers accepting coffee house coupons.

# Summary and Findings
A brief cleaning of the data was included before assessing workable data, rows that were rendered unusable (by having NaN data) were dropped. After data was cleaned, the following was discovered:

The acceptance rate is most impressive for males (likely students) in the age group below 21 (acceptance rate=81.9%) compared to an acceptance rate of 0.483 for all others.

Drivers with monthly coffee house visits of 1~3 times or more had a higher coupon acceptance rate (acceptance rate=65.9% vs 34% for all others)

Drivers with no urgent destination had a higher coupon acceptance rate (acceptance rate = 57.8% vs 40.1% for all others)

Mid morning (10 am) and mid-afternoon (2 pm) times are associated with better acceptance rate of 59.3% versus an acceptance rate of 42.5% earlier in the day (7 am) or later in the evening/night (6 pm, 10 pm)

We found that indeed when all five of the high-likelihood acceptance criteria (age below 50, travelling with friend(s)/partner, number of monthly coffee house visits 1~3 times or more, 1 day expiration of coupons and time of the day being 10 AM or 2 PM) are simultaneously applied, the acceptance rate is very high (82.4%) vs an acceptance rate of only 47.8% for all others. However, there are certain other age groups or demographics that have a high acceptance rate under certain conditions. For example,for drivers who reported their monthly frequency of coffee house visits as less than 1, coupons targeted to male drivers in this category may have a better acceptance rate than females.

Other important insights identified from the above analysis:

Even though acceptance rate of coupons on cold (30 degrees or less) days is lower (44%), there are demographic groups with age over 50 years or male drivers below 21 years where acceptance rate of coupons is much higher (60%) on these cold days

Early morning (7 AM) acceptance rate of coffee house coupons is low (44%). However, the 7 AM acceptance rate for the age group below 21 years is relatively high (69.4%).

# Observations
Which drivers should be targeted for coffee house coupons based on attributes associated with higher acceptance rates?
Based off findings, coffee house coupons should be targeted to drivers below 50 years in age, drivers who are travelling with friend(s) or partner, who report 1 or more monthly visits to coffee houses. The best time of the day for getting a higher acceptance rate is mid-morning (10 AM) or mid-afternoon (2PM).

Which attributes are associated with a low likelihood of acceptance of coffee-house coupons?
Those drivers who report never frequenting a coffee shop have an obviously low likelihood of accepting coffee house coupons. Cold temperature (30F) is also associated, in general, with a lower acceptance of coupons for most drivers excluding males below 21 years and the 50 plus age group. Certain times of day, e.g. early in the morning (7 AM) or later in the evening/night (6 PM, 10 PM) are also associated with a lower likelihood of acceptance.

Which drivers should be targeted for getting a better acceptance rate for certain contextual or coupon attributes that are generally associated with an overall lower acceptance rate?

On cold temperature (30 degree) days, coupons should be targeted to the following demographic groups: age over 50 or males below 21 years. Similarly, 2-hour expiry coupons should be targeted to the particular demographic group of males below 21 years. Coupons in the early morning (7 AM) should be targeted to the age group below 21 years for a better acceptance rate at this time of the day. For drivers who report visiting coffee house less than once a month, coupons should be targeted to male drivers for a better acceptance rate.
