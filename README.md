# tableau

LOD for hourly horizontal split:
sum([deliveries]) / sum({exclude [dsa_hour_of_day]: sum([deliveries])})
