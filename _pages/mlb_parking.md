---
permalink: /mlb_parking/
title: "Real-time On-Street Parking Recommendation Engine"
---

> Winner of Sustainable Award <cite><a href="https://codingfestsydney.github.io/" target="_blank">Coding Fest 2021 @USYD</a></cite>

<a href="https://github.com/jhnliu/melbourne_live_parking/blob/master/Coding-Fest-2021_Poster-Parking-Prediction_10052021.pdf" target="_blank">Poster available</a>

## Introduction 
WHAT IF you know in advance where you can park off-street near your destination?<br>
WHAT IF we guarantee you an off-street parking only 3 minutes walk from your destination?<br>
WHAT IF Google Map directs you to the best parking when you are near your destination?<br>

With real-time parking sensors data released by the City of Melbourne (<a href="https://data.melbourne.vic.gov.au/Transport/On-street-Parking-Bay-Sensors/vh2v-4nfs" target="_blank">link</a>), we created a recommendation system to help drivers navigate to the most satisfying off-street parking bay. Using deep learning model, our system not only considers distances, cost and restriction but also predicts how likely you can park at an off-street bay near your destination. We hope to start a Proof-of-concept that can improve traffic in busy suburbs and reduce air pollution by directing vehicles.

{% include figure image_path="/assets/images/mlb_parking.png" alt="User Interface" caption="Result shown to users after entering the destination." %}

## Requirements
- Python 2.7+
- Flask 2.0+
- MongoDB 4.0

## How do we rank a parking spot?
1. Close to the destination
2. Better price
3. Free of restriction (you can park longer)
4. High probability to park the car (work in progress)

## Future Work
- Continue to improve UI
- Add car park commercial car park information
- Online allocation to prevent multiple drivers competing the same parking bay
