<h1>Pakistan Used Car Market Intelligence</h1>
<h2>Description:</h2>
In Pakistan’s secondary automotive sector where volatile exchange rates, shifting import duties, and high financing costs heavily distort vehicle valuations pricing and inventory decisions are historically driven by dealer intuition rather than empirical market signals. This project aims to move vehicle purchase from intuition to an informed decision. To analyze 10,589 PakWheels listings (median price 34.3 lac, median mileage 88,843 km) to build an interactive Tableau pricing and liquidity engine; isolated 774 mispriced outlier listings (7.3%), quantified the 3-to-5-year depreciation cliff (~80 lac to ~45 lac), and identified a 66.0% automatic transmission shift to guide dealership inventory allocation and trade-in valuation.
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
<h3>Importing Libraries and Loading the Dataset</h3>

<ul>
    <li>Imported Pandas and NumPy for data manipulation and numerical operations.</li>
    <li>Used Matplotlib and Seaborn for statistical visualization.</li>
    <li>Loaded the PakWheels dataset into a Pandas DataFrame.</li>
    <li>Created a separate working copy to preserve the original dataset.</li>
</ul>
<p align="center">
<br/>
<img src="https://user34869.na.imgto.link/public/20261118/2cc36a32889d7c3649a8f006-screenshot-2026-11-18-at-11-28-18-pm.avif"/>
<br />
<br />
<img src="https://cdn.phototourl.com/anon/2026-11-18-02569531-7b4b-415f-a82e-3b29469b73cb.png"/>
<br />
<br />
 <h3>Data Audit and Quality Assessment</h3>

<ul>
    <li>Examined dataset dimensions, column names, data types, and memory information using <code>df.info()</code> and <code>df.shape</code>.</li>
    <li>Identified missing values across individual columns.</li>
    <li>Checked for duplicate records; no duplicate rows were identified.</li>
    <li>Generated descriptive statistics to understand numerical variables.</li>
    <li>Examined unique value counts to assess categorical consistency.</li>
    <li>Investigated 10 implausible engine capacity records and 102 missing engine capacity values to understand their distribution and possible causes.</li>
</ul>
<img src="https://cdn.phototourl.com/anon/2026-11-18-a3cf1c6d-1606-4154-b694-aca11f6c747f.png"/>
<br />
<br />
<img src="https://cdn.phototourl.com/anon/2026-11-18-a20e8de0-6ec1-4e60-8ea3-72253b9c5a7d.png"/>
<br />
<br />
<img src="https://cdn.phototourl.com/anon/2026-11-18-7e31581d-b6fa-469e-85e3-2de68fd9d7a9.png"/>
<br />
<br />  

<h3>Data Inspection and Redundancy Removal</h3>

<ul>
    <li>Inspected the vehicle title column and identified that all 10,589 listings contained the redundant phrase "for sale".</li>
    <li>Removed the redundant phrase using Pandas string operations.</li>
    <li>Compared vehicle titles against structured attributes, including brand, model, variant, and manufacturing year.</li>
    <li>Investigated 548 missing variant values and confirmed that these listings did not specify a variant in their original titles.</li>
    <li>Dropped the title column because its information was largely represented by the structured attributes.</li>
</ul>
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
<h3>4. Exploratory Data Analysis (EDA)</h3>

<ul>
    <li>Selected four numerical variables for univariate analysis: Price (PKR), Manufacturing Year, Mileage (KM), and Engine Capacity (CC).</li>
    <li>Generated descriptive statistics to examine mean, median, standard deviation, and distribution ranges.</li>
    <li>Used histograms and KDE curves to visualize numerical distributions.</li>
    <li>Examined skewness and the influence of extreme observations on central tendency.</li>
    <li>Interpreted distribution patterns to identify market concentrations and potential business implications.</li>
</ul>
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
<h3>Standardization of Data Quality Flags</h3>

<ul>
    <li>Standardized the <code>price_outlier_flag</code>, <code>mileage_flag</code>, and <code>engine_cc_flag</code> columns.</li>
    <li>Filled missing flag values with False and converted the columns into Boolean data types.</li>
    <li>Created a consolidated <code>is_clean_record</code> indicator to identify records that passed all three data quality checks.</li>
    <li>Prepared the quality indicators for filtering and analysis in Tableau.</li>
</ul>

<br />
<br />
<img src="https://user34869.na.imgto.link/public/20261118/d7a081bf5dfef34ca5baf3a4-screenshot-2026-11-18-at-11-18-56-pm.avif"/>
<img src="https://user34869.na.imgto.link/public/20261118/f632f66ac5f224f04568e865-screenshot-2026-11-18-at-11-19-16-pm.avif"/>
<br />
<br />
<h3>Feature Engineering</h3>

<ul>
    <li>Converted the <code>scraped_at</code> column into a datetime format.</li>
    <li>Converted manufacturing year into a nullable integer data type.</li>
    <li>Calculated vehicle age using the difference between listing scrape year and manufacturing year.</li>
    <li>Converted vehicle prices from PKR into PKR Lakhs for more readable dashboard presentation.</li>
</ul>
<h3>Data Type Standardization</h3>

<ul>
    <li>Converted mileage and engine capacity into nullable integer data types.</li>
    <li>Ensured numerical fields were appropriately formatted for business intelligence tools.</li>
    <li>Reviewed final column data types to verify consistency.</li>
</ul>


<img src="https://user34869.na.imgto.link/public/20261118/6ec9158b22302c6b5cbea631-screenshot-2026-11-18-at-11-19-34-pm.avif"/>
<img src="https://user34869.na.imgto.link/public/20261118/40954ec9d7f159f33a6e4d6a-screenshot-2026-11-18-at-11-19-49-pm.avif"/>
<br />
<br />
<h3>Exporting the Tableau-Ready Dataset</h3>

<ul>
    <li>Exported the processed dataset into CSV format.</li>
    <li>Preserved the original dataset by performing all transformations on the working copy.</li>
    <li>Generated a final dataset containing engineered features and data quality indicators.</li>
    <li>Reported the total number of exported records and the proportion of records passing all three quality checks.</li>
    <li>Prepared the resulting dataset for interactive dashboard development in Tableau.</li>
</ul>
<h3>A snapshot of Dashboard</h3> 
<img src="https://user34869.na.imgto.link/public/20261118/32a67b8ccf7b33fbede70c3e-screenshot-2026-11-17-at-4-21-35-pm.avif"/>
<br />
<br />

<section class="business-impact">
  <h2>Business Impact </h2>
  <ul>
    <li>
      <strong>Arbitrage &amp; Mispricing Detection:</strong> Isolated <strong>774 price outliers (7.3% of 10,589 listings)</strong> deviating from the price-to-mileage decay curve, enabling dealers to acquire undervalued stock and flag overpriced inventory before it stalls.
    </li>
    <li>
      <strong>High-Liquidity Inventory Targeting:</strong> Identified peak market volume in the <strong>34.3–35.6 lac median price tier (2,595 listings)</strong>, allowing dealerships to concentrate working capital on fast-turning inventory rather than slow-moving <strong>78.5+ lac</strong> stock.
    </li>
    <li>
      <strong>Depreciation Risk Mitigation:</strong> Quantified an aggressive initial value drop from <strong>~80+ lac down to ~45–50 lac</strong> within the first 3–5 model years, giving auto-leasing firms and trade-in desks precise thresholds for residual value modeling.
    </li>
    <li>
      <strong>Procurement &amp; Powertrain Alignment:</strong> Revealed <strong>66.0% automatic transmission dominance</strong> alongside <strong>Toyota, Suzuki, and Honda</strong> market leadership, guiding inventory buyers to prioritize high-demand automatic variants around the <strong>88,843 km median mileage</strong> benchmark.
    </li>
    <li>
      <strong>Regional Supply Optimization:</strong> Mapped heavy listing concentration across the <strong>Central/Northern Punjab corridor</strong> and <strong>Karachi/Hyderabad</strong>, enabling multi-city dealers to transfer excess stock from saturated metro hubs to underserved secondary markets.
    </li>
  </ul>
</section>




