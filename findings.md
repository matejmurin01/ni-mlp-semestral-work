# Findings of data exploration

- column **nick** can be dropped

## 1. Data cleaning

- only 1 record with missing **num_blocked_shots**, **faceoff_wins**, **faceoff_losses**
-     the record might be corrupt, so it was dropped
- column **shoot_success_rate** inconsistent
-     some players with 0 shots on goal have the success rate at 0 but should be NaN, so it was set as such
- same with **faceoff_success_rate**
- only 1 record with **age** of 0
-     as we don't know if anything else with this record is wrong as well, it was dropped
- there are 2 records with **average_time_on_ice** not set properly
-     we recalculate it as **time_on_ice** / **games_played**
- other constrains check have passed

## 2. Data visualization
- maybe ignore players with too few games/too few shots etc for certain variable statistics, as those might heavily skew the pattern in the data


