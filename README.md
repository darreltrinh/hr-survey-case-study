# hr-survey-case-study
Mock Data used to understand user behavior behind an email campaign related to collecting data regarding an HR survey. 

## Business Problem
Hypothesis: Original Email Campaign wasn't successful as more emails were sent repeatedly to users there was a degredation in users engaging with the platform farther down the line.

The product engages with users in two ways:

* Product Dashboard that displays KPIs generated from anonymous data
* Emails sent to user to prompt a call to action
  * Analysis will center around Email Click Through Rate as we are trying to optimize engagement with the actual product

## Rationale
* Broke down email engagement across the cohort of users and logged emails & subsequent user events to understand the click through rate
  * If users clicked on the email the assumption is that they are interested in engaging with the product's dashboard
* Understand Dashboard Engagement data as it relates to the email data
  * Of the users that received the emails, how did this affect their journey? Are the emails creating more subsequent engagement in the product's user experience
* Since emails are the primary interaction that users receive outside of the product - are there different variables we can test to isolate why the original email campaign wasn't successful?

## TL;DR of findings
* Campaign wasn't successful based on data exploration that showed a negative correlation with amount of emails sent to user vs. click through rate to platform
* Macro-level analysis across all users show sustained interest. So users are interested in the content being supplied to them by platform.
  * This means there is a degradation in user experience outside of platform as communications come in from the product to trigger engagement.
* Of the users identified ~80% of them engaged with the dashboard at some point in time during the email campaign.
  * Recommend enriching with web analytics data to understand user telemetry to refine the next hypothesis for testing
* Recommendation based on data provided:
  * Updated Hypothesis: By optimizing the communications from the product to a time where users' are more likely to interact with external product emails will increase the engagement within the application.
  * A/B test on the time the email is sent on Tuesday, as it is the day the product receives highest engagement, but test on time the email is sent out.
    * A: Sent at 9 AM - Tuesday
    * B: Sent at 6 PM - Tuesday
      * Tuesday @ 6 showed the greatest amount of engagement in the email campaign
    * Testing to see if the user is more likely to engage at the start of the day
      * Web analytics data would be helpful here to see where the drop off is in the user workflow.
      
## Potential Enhancements:
* Use data to build a propensity model for user's likelihood to click through the email sent
  * Opens up door for programmatic engagement based on user to increase engagement
* enrich with web analtyics data to inform product of core features to build/refine workflows for user
* cohorting users by onboarded month of org vs actual user engagement to understand adoption of product within client org.
