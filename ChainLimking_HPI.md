When transitioning from the older 2010–11 series to the updated 2022–23 base series for the RBI House Price Index (HPI), direct data linking becomes inherently problematic. The 2022–23 series represents a structural overhaul: the RBI expanded its geographic coverage from 10 major metropolitan centers to 18 major cities, altered the relative weights of those cities, and adjusted for a post-pandemic economic environment. [1, 2, 3, 4] 
Because the underlying "basket" and city composition changed significantly, standard statistical methods must be applied carefully. Financial institutions and central banks rely on specific statistical techniques to handle these distinct, non-overlapping index revisions. [5] 
------------------------------
## 1. Splicing Techniques (The Central Bank Standard)
When the RBI or the Ministry of Statistics and Programme Implementation (MoSPI) introduces a fundamentally different base year, they do not merge the raw datasets. Instead, researchers use statistical splicing to create a continuous historical time series. Two methods can resolve this issue: [5, 6] 

* Forward Splicing (Splicing Old to New):
This method expresses the historical data in terms of the new 2022–23 base year. You take the old index value at the overlapping period and multiply it by a calculated conversion factor.
$$\text{Conversion Factor} = \frac{\text{New Index Value at Overlap Period}}{\text{Old Index Value at Overlap Period}}$$ 
Every historical data point in the 2010–11 series is then multiplied by this conversion factor to rescale the historical data backward.
* Backward Splicing (Splicing New to Old):
If your existing research models are entirely built around the 2010–11 base year, you can project the new 2022–23 data backward. The inverse of the conversion factor is applied to the new data points to keep the historical baseline unchanged.

## 2. The Multi-City Overlap Challenge
The 2022–23 series introduces an operational bottleneck: it covers 18 cities (adding major hubs like Hyderabad, Pune, and Thane), whereas the 2010–11 series only tracked 10 cities. [1, 2, 4] 
To chain-link these series effectively, you cannot use the aggregated "All-India HPI" directly because you would be comparing a 10-city aggregate to an 18-city aggregate. Instead, the standard research approach is to: [1, 2] 

   1. Isolate the 10 overlapping cities common to both series ([Ahmedabad](https://www.google.com/search?kgmid=/m/01d88c), [Bengaluru](https://www.google.com/search?kgmid=/m/09c17), [Chennai](https://www.google.com/search?kgmid=/m/0c8tk), [Delhi](https://www.google.com/search?kgmid=/m/09f07), [Jaipur](https://www.google.com/search?kgmid=/m/016722), [Kanpur](https://www.google.com/search?kgmid=/m/01_q7h), [Kochi](https://www.google.com/search?kgmid=/m/0fl2s), [Kolkata](https://www.google.com/search?kgmid=/m/0cvw9), [Lucknow](https://www.google.com/search?kgmid=/m/022tq4), and [Mumbai](https://www.google.com/search?kgmid=/m/04vmp)).
   2. Apply individual, city-level forward/backward splicing to those 10 specific cities.
   3. Re-weight those 10 cities manually if you need a customized, historical "Top-10 Metro Index" spanning from 2010 through the current period. [1] 

## 3. Splicing at the Growth Rate (The Econometric Approach)
If the structural adjustments made to the 2022–23 series create an unacceptable mathematical jump in the absolute index values, econometric research mandates shifting the baseline to Growth Rates ($Y\text{-}o\text{-}Y$ or $Q\text{-}o\text{-}Q$) rather than absolute index points.
Because the index values themselves are arbitrary markers relative to a base year, tracking the underlying percentage changes eliminates base-year distortion. You can link the series by appending the quarterly growth rates of the 2022–23 series directly onto the historical growth rate timeline of the 2010–11 series. [7] 
------------------------------
## Summary Recommendation for Your Model

* Avoid splicing the national "All-India HPI" directly. The structural change in the number of cities will invalidate the historical comparison.
* Download the city-level datasets from the RBI Database on Indian Economy (DBIE).
* Use Forward Splicing on a city-by-city basis for the 10 overlapping cities, using the overlapping quarters of the financial year 2022–23 to establish your conversion coefficients. [1, 4] 

If you want to dive deeper into the mathematics, I can provide the exact step-by-step formula for forward splicing using a hypothetical data example. Would you like me to walk through a calculation using real or sample numbers for a specific city?

[1] [https://docs.publicnow.com](https://docs.publicnow.com/viewDoc.aspx?filename=8151%5CEXT%5CFD809C084BE5BF0DC54D04957FD2F3F48988E483_545B8079B7D116B7FC0BB484EAC0C917D9579938.PDF)
[2] [https://www.business-standard.com](https://www.business-standard.com/industry/news/india-s-house-price-index-rises-2-2-in-q2-as-rbi-updates-base-year-125112700977_1.html)
[3] [https://www.drishtiias.com](https://www.drishtiias.com/daily-updates/daily-news-analysis/indias-new-gdp-series-with-base-year-2022-23)
[4] [https://www.policyedge.in](https://www.policyedge.in/p/rbi-releases-new-house-price-index)
[5] [https://www.youtube.com](https://www.youtube.com/watch?v=PX5pIc0ImYM)
[6] [https://www.pib.gov.in](https://www.pib.gov.in/PressReleasePage.aspx?PRID=2233518&reg=3&lang=1)
[7] [https://www.aurumproptech.in](https://www.aurumproptech.in/pulse/blog/house-price-index-in-india)
