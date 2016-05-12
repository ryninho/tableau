# tableau

LOD for hourly horizontal split:
sum([deliveries]) / sum({exclude [dsa_hour_of_day]: sum([deliveries])})

correction for multiple rows per zone id (want sum of forecasted demand across zones despite duplicate rows by zone, to compare to unique basis dates' actual demand):
sum({fixed [zone_id], [future_date]: avg([forecasted_demand])})
