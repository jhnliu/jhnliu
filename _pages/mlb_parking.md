---
permalink: /mlb_parking/
title: "Real-time On-Street Parking Recommendation Engine"
---

# Introduction 

WHAT IF you know in advance where you can park off-street near your destination?<br>
WHAT IF we guarantee you an off-street parking only 3 minutes walk from your destination?<br>
WHAT IF Google Map directs you to the best parking when you are near your destination?<br>

With real-time parking sensors data released by the City of Melbourne ([source]: https://data.melbourne.vic.gov.au/Transport/On-street-Parking-Bay-Sensors/vh2v-4nfs), we created a recommendation system to help drivers navigate to the most satisfying off-street parking bay. Using deep learning model, our system not only considers distances, cost and restriction but also predicts how likely you can park at an off-street bay near your destination. Our team hope to start a Proof-of-concept that can improve traffic in busy suburbs and reduce air pollution by directing vehicles.

{% include figure image_path="/assets/images/mlb_parking.png" alt="User Interface" caption="Result shown to users after entering the destination." %}

# Future Work
- Continue to improve UI
- Add car park commercial car park information
- Online allocation to prevent multiple drivers competing the same parking bay
