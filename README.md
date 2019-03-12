# API Production Forecast Reports

This report may be used to help forecast production requirements for styles based on previous sales history and a pre-defined replenishment code and percentage.

Pre-requisites for running this report:

Users must complete the following steps:
1. Ensure that replenishment codes have been set up in their system under Setup > Codes > Replenishment Codes Tab.
2. Using the global Changes Styles Module under Modules > Styles, users must apply a replenishment code to all Styles where a replenishment forecast is desired.

Once the above steps are completed, the report will accurately forecast production needs based on prior sales time period selection, provided replenishment code and any additional criteria in use.

Additional Criteria Selections:

Increase forecast by % - will increase the replenishment forecasted by an additional % if entered.
Exclude open Bulk Orders - will exclude any remaining open balance on a bulk order.
Consider minimum stock of a style - if a minimum stock is set, the forecast report will take that into consideration when
providing the forecast numbers (ie: the style forecast will not be below the minimum stock setting)
Include case details will report on the replenishment amount needed for the individual items within any case.
