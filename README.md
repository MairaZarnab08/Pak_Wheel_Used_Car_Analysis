<h1>Pak Wheel used Car Analysis</h1>
<h2>Description:</h2>
This project involves a thorough analysis of 10,589 vehicles listed by Park wheels to uncover pricing trends, depreciation patterns, brand performance and regional market distribution across Pakistan. Data was obtained from Kaggle. After initial data quality check and cleaning the csv file was imported in Tableau for building interactive dashboard. Where 10,589 listed vehicles were analyzed over a time period of 65 years. 
<br />
<br />
<h2>Objectives:</h2>
<ul>
 
  <li>Identify key factors influencing vehicle listing prices.</li>
  <li>Examine vehicle depreciation patterns across over 65 years.</li>
  <li>Compare brand-wise listing volumes and market presence.</li>
  <li>Investigate the relationship between vehicle mileage and price to optimize best deals to purchase.</li>
  <li>Analyze regional distribution of used-car listings across Pakistan.</li>
  <li>Identify pricing outliers and the percentage of Automotive vehicles in the Active listings.</li>
  
</ul>

<h2>Utilities Used:</h2>
<ul>
 <li><b>Visualization tool:</b> Tableau</li>
  <li><b>Programming Language:</b> Python</li>
  <li><b>Libraries:</b> Pandas, NumPy, Matplotlib, Seaborn</li>
</ul>

<h2>Dash Board Featurers:</h2>
<ul>
  <li>KPI cards showing Active listings, Median mileage, Median price, Automatic share and Price outliers.</li>
  <li>No of vehicles for top 10 brands and depreciation over a period of 66 years.</li>
  <li>Regional map showing active listings for sale across 193 cities of Pakistan.</li>
  <li>Pie charts showing median price per age category and Active listings per age bracket.</li>
  <li>4 filters allowing the stakeholders to see the feature distributions across Year span.Engine category, Fuel type and Transmission.</li>
</ul>
<h2>Program walk-through:</h2>
<p align="center">
<br/>
<img src="https://user34869.na.imgto.link/public/20261118/2cc36a32889d7c3649a8f006-screenshot-2026-11-18-at-11-28-18-pm.avif"/>
<br />
<br />
<img src="https://cdn.phototourl.com/anon/2026-11-18-02569531-7b4b-415f-a82e-3b29469b73cb.png"/>
<img src="https://cdn.phototourl.com/anon/2026-11-18-a3cf1c6d-1606-4154-b694-aca11f6c747f.png"/>
<br />
<br />
<img src="https://cdn.phototourl.com/anon/2026-11-18-a20e8de0-6ec1-4e60-8ea3-72253b9c5a7d.png"/>
<br />
<br />
<img src="https://cdn.phototourl.com/anon/2026-11-18-7e31581d-b6fa-469e-85e3-2de68fd9d7a9.png"/>
<br />
<br />  
<img src="https://user34869.na.imgto.link/public/20261118/7089630502dccbb91cfc1d4d-screenshot-2026-11-18-at-11-29-34-pm.avif"/>
<br />
<br />
 <img src="https://user34869.na.imgto.link/public/20261118/e6c94b7c01066d24ef6f4170-screenshot-2026-11-18-at-10-45-45-pm.avif"/>
<br />
<br />
 <img src="https://user34869.na.imgto.link/public/20261118/8ae799b0ac7ada0ac97c8030-screenshot-2026-11-18-at-10-45-58-pm.avif"/>
<br />
<br />
<img src="https://user34869.na.imgto.link/public/20261118/5e871f4faec381522e51f9d0-screenshot-2026-11-18-at-10-46-10-pm.avif"/>
<br />
<br />
<img src="https://user34869.na.imgto.link/public/20261118/62227c6a7644e633d721d851-screenshot-2026-11-18-at-11-15-12-pm.avif"/>
<img src="https://user34869.na.imgto.link/public/20261118/55657e462c686ee169e19062-screenshot-2026-11-18-at-11-14-22-pm.avif"/>
<br />
<br />

 <h3>1. Price (PKR)</h3>

<ul>
    <li>Strong positive (right) skewness.</li>
    <li>Most listings are concentrated in the lower price ranges.</li>
    <li>A small number of expensive vehicles extend the distribution towards PKR 108 million.</li>
    <li>The mean is therefore higher than the median.</li>
    <li><strong>Business implication:</strong> Median price may be a more representative measure of typical listing prices than mean price.</li>
</ul>

<h3>2. Manufacturing Year</h3>

<ul>
    <li>Listings are concentrated around 2010–2022.</li>
    <li>2020 appears to have particularly high listing frequency.</li>
    <li>Older vehicles represent a relatively small proportion of listings.</li>
    <li><strong>Business implication:</strong> The dataset is dominated by relatively newer vehicles.</li>
</ul>

<h3>3. Mileage</h3>

<ul>
    <li>Most vehicles have mileage below approximately 200,000 km.</li>
    <li>The distribution is positively skewed.</li>
    <li>A few listings have extremely high mileage, reaching nearly one million kilometres.</li>
    <li><strong>Business implication:</strong> Mileage segmentation could help explain differences in vehicle pricing.</li>
</ul>

<h3>4. Engine Capacity</h3>

<ul>
    <li>Most vehicles fall between 660 cc and 2,000 cc.</li>
    <li>There are noticeable concentrations around 1,000, 1,300 and 1,500 cc.</li>
    <li>Larger-engine vehicles are comparatively less common.</li>
    <li><strong>Business implication:</strong> The market appears concentrated around small- and medium-engine-capacity vehicles.</li>
</ul>
<br />
<br />
<img src="https://user34869.na.imgto.link/public/20261118/d7a081bf5dfef34ca5baf3a4-screenshot-2026-11-18-at-11-18-56-pm.avif"/>
<img src="https://user34869.na.imgto.link/public/20261118/f632f66ac5f224f04568e865-screenshot-2026-11-18-at-11-19-16-pm.avif"/>
<br />
<br />
<img src="https://user34869.na.imgto.link/public/20261118/6ec9158b22302c6b5cbea631-screenshot-2026-11-18-at-11-19-34-pm.avif"/>
<img src="https://user34869.na.imgto.link/public/20261118/40954ec9d7f159f33a6e4d6a-screenshot-2026-11-18-at-11-19-49-pm.avif"/>
<br />
<br />
<img src="https://user34869.na.imgto.link/public/20261118/32a67b8ccf7b33fbede70c3e-screenshot-2026-11-17-at-4-21-35-pm.avif"/>
<br />
<br />






```
--!>






<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
