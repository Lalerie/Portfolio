# A/B testing

[.md](https://choosealicense.com/licenses/mit/)
[.ipynb](https://choosealicense.com/licenses/mit/)

## Research purpose

Evaluate the results of the A/B test.

### Technical specification
    
- Test name: `recommender_system_test`;
- groups: A — control, B — new payment funnel;

- audience: 15% of new users from the EU region;
- purpose of the test: testing of changes related to the implementation of an improved recommendation system;
- expected number of test participants: 6000;
- expected effect: in 14 days from the moment of registration, users will show an improvement in each metric by at least 10%:
    - conversions to viewing product cards — the `product_page` event,
    - basket views — `product_cart`,
    - purchases — `purchase'.

## Research description

`ab_project_marketing_events.csv` — calendar of marketing events for 2020.
- `name` 
- `regions` 
- `start_dt`
- `finish_dt` 
`final_ab_new_users.csv` — users registered from December 7 to December 21, 2020.
- `user_id`
- `first_date`
- `region`
- `device`
`final_ab_events.csv` — actions of new users in the period from December 7, 2020 to January 4, 2021.
- `user_id` 
- `event_dt` 
- `event_name` 
- `details` 
- `purchase` 
`final_ab_participants.csv` — table of test participants.
- `user_id` 
- `ab_test` 
- `group`

## Project summary 

Comparison of funnels shows that the conversion in test group B has worsened in two stages. 
This may be due to the intersection with the holidays, the incompleteness of the test - the set of users was completed later by 2 days and the test was stopped earlier by 5 days, which ultimately excludes most of the users from consideration. Also on December 13, there was a sharp jump in the number of events in Group A.

According to the results of the test, there are significant differences between the conversion of groups to "product_page" and "purchase".  

There are also significant differences in the number of events per user between groups - the relative gain of group A is 17%.   

These results should not be guided, since the test was conducted incorrectly, most of the points of the TOR are not observed.

It is recommended to conduct the test again in compliance with the terms of the TOR, outside of festive promotions.