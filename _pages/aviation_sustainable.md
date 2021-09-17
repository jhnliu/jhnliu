---
permalink: /unsw_ds/
title: "Sustainable International Air Routes to Australia "
---

> Best Insight Award & Best Visualization Award - UNSW Data Science Competition

## Data Science Competition on "Sustainable International Air Routes to Australia" 
Tourism Australia and UNSW School of Aviation, in partnership with Cirium, is organising a Data Science Competition on "Sustainable International Air Routes to Australia" (<a href="https://www.aviation.unsw.edu.au/data-science-competition">link</a>).<br>
<br>
To better understanding of how international air travel play a role in promoting a more sustainable tourism destinations in air travel dependent tourism regions, our team used the given data to identify international air routes to Australia that are likely most sustainable in the post-COVID travel environment. Cirium’s select origin-destination data includes seat capacity, traffic, aircraft type and future schedules.We also made use of multiple external datasets from Australian Bureau of Statistics, flight manager, myclimte, etc.<br>
<br>
Our team approached the problem from 3 perspectives: Economy, Covid Recovery and Environment. In this article, I will share my findings and work in the Environment perspective.
<br>

# Process
### Step 1 - Define the problem and objective
To evaluate the carbon footprint of the routes, we collect the carbon emission per traveller from <a href="https://co2.myclimate.org/en/flight_calculators/new">myclimate flight calculators</a> and normalised it by the route distance to get a carbon emission score. The lower the score, the more environmental friendly the route is. Here, we only consider a one-way flight to keep things simple.

{% include figure image_path="/assets/images/unsw_ds/formula.jpg" alt="carbon emission formula" caption="Slide created by Zoe Lo" %}

### Step 2 - Prepare the data (Webscraping, data wrangling)
Having the objective, it is time to collect the data. Our given dataset contains all origin and destination that we had to consider. To collect the carbon emission data, we scrape it from myClimate using <a href="https://www.selenium.dev/">Selenium</a> and stored the corresponding O/D and emission in a dataframe, using pandas. Next, we performed an inner join on the origin column to get the complete dataset with necessary information.

### Step 3 - Find insights and show with visualizations

Using Tableau, we managed to create several visualizations and derive insights from them. We matched our airport code to the coordinates on the world map to visualize the information in a geographical context.

{% include figure image_path="/assets/images/unsw_ds/best_worst.jpg" alt="best worst 10" caption="Top 10 and Bottom 10 routes ranked by carbon emission per km" %}

From the visualisations, we observed that carbon-friendly flights are not limited to short-haul flights, for example, LHR-MEL is the top 5 environmental-friendly route. Besides, at a similar flight distance, some routes have relatively higher emission due various factors such as aircraft type, airport infrastructure and cargo loading.

{% include figure image_path="/assets/images/unsw_ds/insight.jpg" alt="carbon emission insight" caption="" %}

Among all routes in the dataset, routes originated from several airports are generally more carbon friendly. For example, all flights from Kuala Lumpur International Airport (graph on the left) are relatively carbon friendly. On the other end, routes from Honolulu airport (graph on the right) are relatively less carbon friendly. This echoes the airport infrastructure factor in the carbon emission formula from myclimate. Therefore, we suggest airline company to consider not only distance but also airport operations when they look at the carbon emission of a route.

## Reference
The myclimate Flight Emission Calculator 
https://www.myclimate.org/fileadmin/user_upload/myclimate_-_home/01_Information/01_About_myclimate/09_Calculation_principles/Documents/myclimate-flight-calculator-documentation_EN.pdf

## Prize Presentation
{% include figure image_path="/assets/images/unsw_ds/unsw_ds_photo.jpg" alt="carbon emission insight" caption="" %}




