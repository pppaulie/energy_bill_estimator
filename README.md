# energy_bill_estimator
Energy Bill Estimator - Custom Component - Home Assistant

This custom Home Assistant component estimates the end-of-month energy bill based on user-configurable parameters. It allows users to either select existing entities (like sensors or input numbers) or enter custom values directly in the UI. Here’s a breakdown of its functionality:

User Configuration: Users can configure the following values through the UI:

Daily Supply Cost: Either enter a fixed daily cost or select an entity providing this cost.
Cost per kWh: Enter a fixed rate or select an entity for the price per kilowatt-hour.
Current Monthly Usage Cost: Enter a custom value or select an entity tracking the current monthly usage.
Days in Billing Cycle: Set the number of days (defaulted to 31).
Calculations:

Supply Cost: Multiplies the daily supply cost by the number of days in the billing cycle to get the projected total supply cost for the month.
Usage Cost: Calculates the average daily usage cost by dividing the current monthly usage cost by the days passed in the billing cycle. This average is then multiplied by the total days in the cycle to project the monthly usage cost.
Total Estimated Cost: Adds the supply cost and the projected usage cost to estimate the end-of-month bill.
Automatic Updates: The sensor updates regularly, recalculating the projected cost as the current usage and daily parameters change throughout the billing cycle.

Customizable through UI: Users can adjust settings without modifying code, making it adaptable and user-friendly.

Overall, the component provides a running estimate of the monthly bill, updating as the month progresses based on current usage trends and specified parameters.

-------------------------------------------------------------------------
This is how the wizard appears - unfortunately I am having difficulty with adding destriptive text.
![image](https://github.com/user-attachments/assets/46ddb6c3-e5b9-4e9e-85fe-80a9db3dc1b3)


This is how it should (will one day) look:
![image](https://github.com/user-attachments/assets/c49923af-9917-4d79-b70a-096883f6bfa4)
