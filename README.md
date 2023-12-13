#### Motivation: Explore Restaurants (20-50) coupon group
In the notebook, we narrowed our focus on the coupon categories that are harder to push (other than bar coupons) and explore the differences in those who accept and reject the coupon.

Since more expensive restaurants (ie. Restaurants (20-50)) has the second lowest acceptance rate, we will focus on cracking this tougher nut with some slicing and dicing.

The intention will be to identify factors which increase likelihood of drivers accepting this coupon type.

#### Findings from Bar Plots
To keep laser focus through the noise, we make notable observations for where acceptance rate is above the population's acceptance rate of 0.44.

When do we see increases in coupon acceptance? When:

Contextually
- the destination is 'no urgent place' (0.50)
- their 'partner' is the passenger (0.63)
- the weather is sunny it marginally improves to 0.46
    - likewise when temperature is 80F it improves to 0.48
- the time of the coupon is sent at 10 AM (0.60), followed by 2 PM (0.54)
- the coupon expiration is longer at 1 day (0.52)

Demographically
- the driver is male (0.46)
- the driver is between the ages of 26 - 46 (~0.5)
- the marital status is single or unmarried partner (~0.47)
- the driver has no children (0.47)
- their education is a high school graduate or some high school (0.52 to 0.58)
- the occupation is in construction & extraction (0.62), healthcare support (0.66), healthcare practictioner (0.57), office and admin support (0.62), and production occupations (0.73)
- income over 100K (0.50) or between 25 to 50K (0.53)

Behaviourally
- the driver visits bars or restauraunts at least once a month: the more frequent the more likely (ie. as high as 0.69 when going to expensive restaurants more than 8 times)

#### Heatmap Findings 1: First bingo!
Looking at the top left quadrant tells us that lower income drivers (under 50K) who go to restauraunts in the 20 to 50 range more than four times a month, have a very high likelihood to accept the coupon (between 0.71 to 0.82)!

#### Heatmap Findings 2: Expiration does play some role
While acceptance rate does increase when a coupon is sent at 10 AM and has a longer expiration (a day), 0.68 just nearly misses our goal to find observations above 0.70.

A surprising twist to our initial hypothesis, perhaps rich people are less enticed by coupons given the relative savings of a coupon is less signifcant?

#### Heatmap Findings 3:  Second bingo!
Bingo and another one in the bag! This time we find a whopping 0.80 acceptance rate when driving with a partner and the coupon is recieved at 2PM.

#### Heatmap Findings 4: Another bingo?
Yes and no. Interestingly in the higher income groups some niche patterns emerge.
- 75K to 87.5K income drivers with children that never eat at expensive restaurants, are very likely to accept the coupon (0.86)
- Drivers with 100K or more income without children that already go more than once a month, are very likely to accept the coupon (0.74 to 0.80)


#### Next Steps and Recommendations
- From our findings, it is clear there are ways to improve which drivers to target to get better traction on accepting more expensive restaurant coupons.
- While not exhaustive, based on our findings the following recommendations can help improve targeting efforts by only prompting drivers with coupons as follows:

    1. **When the time is between 10 AM or 2 PM** (driving with a partner or providing a longer coupon expiration time can further improve the acceptance)

    2. **When the driver's occupation is in anything that makes having prepared-from-home meals during the day difficult** (ie.  production occupations, healthcare support, healthcare practicitioner, construction & extraction)
    
    3. **When the driver is known to already frequent bars or expensive restaurants at least once monthly** (choosing lower income drivers (under 50K) or higher income drivers (over 100K) without children can further improve acceptance)

- Possible next steps include

    1. Investigating the remaining coupon group, coffee house, which also has lower than average acceptance rate.

    2. Producing a machine learning model to help predict and select drivers to present more expensive restaurant coupons to, using the above observations as a starting point for feature selection.

    3. Acquiring additional sample survey data to validate observations with low sample counts at lower granularities