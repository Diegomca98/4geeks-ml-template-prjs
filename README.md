# Exploratory Data Analysis Project

## New York Airbnb EDA solution

**Possible questions to answer:**
* availability_365:
    * What could affect the accomodation demand?
* calculated_host_listings_count:
    * More offer equals to more rentals of the same accomodation?
* number_of_reviews:
    * More reviews equals more rentals?
* minimum_nights:
    * More flexible minimum nights equals more rentals?

**Question to answer:**
* What features affect the availability of the accomodation?

<hr>

### Information about Airbnb
According to the article published by [Tech Crunch](https://techcrunch.com/2023/05/03/airbnbs-average-home-prices-have-gone-up-so-now-its-refocusing-on-rooms-to-give-users-more-affordable-alternatives/) published May 23, 2023 and others like [ThePointsGuy](https://thepointsguy.com/news/airbnb-rate-surge/), at that specific point in time we were seeing a 36% increase on Airbnb rental prices in contrast with 2019.

With this, even before starting our analysis, we can assume that if prices are below the current cheapest accomodation in 2024 minus the 36% price increase is either misinformation or "trash" data.

By doing a quick research on the actual (Airbnb)[www.airbnb.mx] site I concluded that the cheapest accomodations are between **30 USD** and **40 USD** at this time, so substracting the 36% increase we get that the (possible) minimum price per night at that time was **18.56 USD**