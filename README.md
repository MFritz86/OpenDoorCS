# Opendoor Labs Inc. -  Case Study 

## Overview and Origin
Open Door Labs Inc. (dba Opendoor), is a pioneering FinTech company that is reinventing the residential real estate transaction. The company is offerring customers an on-demand, digital experience to buy and sell homes. Opendoor enables homeowners to sell and buy online in a few taps of a button, providing greater simplicity and convenience than the traditional realtor sales transaction model. 

Opendoor is headquartered in San Francisco, California, and was founded in 2014. The founders of the company were Keith Rabois (Executive Chairman), Eric Wu (CEO), Ian Wong (CTO) and JD Ross. Mr. Rabois, managing director at Khosla Ventures, came up with the idea for Opendoor. Since its founding, the company has served over 80,000 customers and sold over $10 billion of homes.

### Capitalization
According to Crunchbase, Opendoor raised $1.5 billion in a series of eight (8) equity capital raises through March 2019. There are approximately 64 investors in the firm with General Atlantic, SoftBank Vision Fund and Lennar Corp. (Lennar), being the largest investors. As the company experienced strong growth during its early formative years, further capital infusions to aid future growth plans are necessary to remain competitive.

### Recent Developments
On September 15, 2020, Opendoor entered into a definitive business combination ageement with Social Capital Hedosophia Holdings Corp. II (NYSE:IPOB)("SCH"), a publicly traded special purpose acquisition company, to bring public a leading digital platform for residential real estate. The contemplated transaction will consist of a combination of stock and cash financing. 

The definitive business agreement calls for the two firms to combine, operating under the Opendoor name, at an enterprise value of $4.8 billion, representing 1.0x 2019 revenue. The transaction is expected to deliver up to $1 billion of gross proceeds including the contribution of up to $414 million of cash held in SCH's trust account from its initial public offerring in April 2020. Further supporting the transaction will be a $600 million Private Investment in Public Equity (PIPE) at $10.00 per share.

The PIPE will be comprised of $100 million from Chamath Palihapitiya, Founder and CEO of SCH, $58 million from Hedosophia and $42 million from Opendoor existing investors, Access Industries, Lennar, along with Opendoor management. The remaining $400 million of PIPE investments include funds and accounts managed by BlackRock (NYSE: BLK), the world's largest asset manager with $7.4 trillion in assets under management, and Healthcare of Ontario Pension Plan (HOOPP), a multi-employer defined benefit pension plan serving more than 381,000 members in the province of Ontario, Canada.  

The transaction will provide up to $1 billion in new liquidity to Opendoor to fund operations and suport new and existing growth plans. Boards of Directors for Opendoor and SCH have approved the transaction which is still subject to approval by SCH's shareholders and other customary closing conditions.

---
## Business Activities
Opendoor 's premise is selling and buying homes the traditional realtor way is time consuming and often complicated process. Potential sales can fall out of escrow and cause significant stress and financial complications for buyers and sellers alike. In addition, showing houses to potential buyers during the COVID-19 pandmeic has introduced new element of risk to completing a sales transaction. 

The traditional realtor approach is often complicated with multiple showings and open houses to market the home. In certain situations, there could be multiple counteroffers between the seller and buyer. The closing process can take up to 90 days posing risk an element of risk from the transaction falling out of escrow.  

### U.S. Residential Real Estate Market
The U.S. residential real estate is an extremely large and highly fragmented industry as evidenced by the following:

1. The market has an estimated $1.6 trillion in annual home sales, 
2. The average home sales are approximately 5.6 million units per year, 
3. There are approximately 1.4 million licensed realtors, and 
4. There are more than 106,000 real estate brokerage firms. 

According to the National Association of Realtors, nearly 48% of all real estate firms cite keeping up with technology as one of the biggest challenges facing their firms in the short to medium term. Many realtors use technology for communications and marketing purposes. The industry appears ripe for disruption by innovative technology. 

### Business Model
The company's business model seeks to engage sellers/buyers of residential real that want to reduce time spent in the sale/buy process, and have certainty of execution in the sales transaction. In addition, the shift from offline to online consumption is accelerating in part due to COVID-19 and by increased customer awareness of this alternative. 

Opendoor's market intelligence indicates consumers are prioritizing safety, demanding digital experiences, seeking to relocate from dense metro areas and searching for larger home sizes to work from home. These transformative trends are creating opportunities for companies, such as Opendoor, whose mission is to empower consumers with the freedom to move.  

Basically, the sell/buy process at Opendoor functions as follows: Homeowners obtain a quote, through an algorithm, and if acceptable elect to sell their houses directly to the company. Sellers get to choose a closing date that fits with their timeframe and closing is finalized by a digital process. 

Upon acquisition by Opendoor, the firm may elect to invest in some upgrades and then put the house on the market to sell. The spread between what the home is bought for and sold is a part of how Opendor generates revenues. It also provides services such as a mortgage product, escrow/title, home repair and home warranty that customers can purchase.  

To meet the challenging landscape due to COVID-19, the company recently announced three new ways to help people sell, or buy, safely with fully digital, contact-free experiences.  These are:
1. Sell Direct - a contact-free way to sell instantly to Opendoor.
2. Home Reserve - A new way to reserve and move into a new home while the company lists an owner's current home.
3. Safer Touring - The ability to virtually tour or self-tour homes to buy.

Home sales can close in as little as two weeks.  An app launched in 2019 enable buyers to schedule self-guided tours and make offers on any home sales in the cities the firm operates.

### Technologies used by Opendoor
#### Product Architecture
The firm uses Puma as their webserver, and Postgres (/postresql) for its database and PostGIS for location data. Sidekiq runs the firms' asynchronous jobs with support from Redis. Elasicsearch is also utlized. Webpack is used to build frontend apps, and serve them using Rails Asset Pipeline. For photos of homes the company uses Imgix.

Where appropriate, the firm tries to break isolated logic into microservices. The transactional cost structure changes frequently and to test how policy changes impact fees. Opendoor uses a version-history-aware computation graph to calculate and back-test internal costs. React frontend will soon help to visualize these calculations. The data science stack is a fully separate set of services with a robust amount of inter-app communication. The firm uses an Elixir app called Paladin to facilitate authentication between services. 

#### Data Science Architecture
Opendoor groups the data science work into serval core areas:

* Ingesting and organizing data from multiple sources.
    * For data ingestion, the company "pulls" data from a variety of sources and stores the data into a RDS Postgres(/amazon-rds-for-postgreql) database. The data is normalized in this phase.

* Training machine learning models to predict home value and market risk.
    * For machine learning, python is used with building blocks for SqlAlchemy, scikit-learn, and Pandas.

* Quantifying and mitigating various forms of risk, including macroecnomic and individual house-liquidity.
    * For routing/handling requests Flask is utlized. Docker is used to build images and Kubernetesnis utilized for deployment and scaling. This automation enables Opendoor to iterate rapidly. Becuase the firm needs to support its more complex algorithms it deploys Dask for fetching and processing.

* Collecting information in a data warehouse to empower the analytics team.
    * For data warehousing, Google's BigQuery is utlized. 

Tool and Workflows - Opendoor manages all of its repositories and code reviews on GitHub. 

---
## Business Landscape
Opendoor operates in the FinTech domain of mortgage/real estate. More specifically, it is an iBuyer of residential real estate. Residential real estate is still dominated by the traditional broker model where most consumers contract with a licensed agent to conduct the marketing and sale of their home.

There are various FinTech business models for the broad domain of mortgage/real estate including, but not limited to: 
1. Mortgage services (e.g., Blend, LendingHome), 
2. Crowdfunding platforms (e.g., Fundrise), 
3. Investment services (e.g., Roofstock), and 
4. Commercial real estate platforms (e.g., Cadre). 
 
However, there are few players offering customers one-stop buying and selling of residential real estate on the scale of Opendoor. The primary competitors to Opendoor are Offerpad, Zillow Offers, Knock and RedFinNow. 

---
### Where iBuyers are operating
Opendoor has the largest national presence and operates in the following 21 metro areas: Atlanta, Austin, Charlotte, Dallas-Ft Worth, Denver, Jacksonville, Houston, Las Vegas, Los Angeles-Orange Couty, Minneapolis-St Paul, Nashville, Orlando, Phoenix, Portland, Raleigh-Durham, Sacramento, San Antonio, and Tucson.

Offerpad, founded in 2015 and headquartered in Chandler, Arizona, operates in the following metro areas: Atlanta, Austin, Birmingham, Charlotte, Dallas Ft-Worth, Houston, Jacksonville, Las Vegas, Orlando, Phoenix, San Antonio, Tampa, and Tucson.

ZillowOffers, an affiliate of the Zillow Group was founded in 2018 and headquartered in Seattle, Washington. The company operates in the following metro areas: Atlanta, Charlotte, Colorado Springs, Dallas, Ft-Worth, Denver, Fort Collins, Houston, Las Vegas, Los Angeles-Orange County, Nashville, Phoenix, Portland, Raleigh-Durham, Riverside County. 

Knock, founded in 2015 and headquatered in New York, the company currently operates in only five metro areas and these are: Atlanta, Charlotte, Dallas, Denver, Phoenix, and Raleigh-Durham.

RedFinNow, founded in 2017 and headquartered in Seattle, Washington, operates in the following markets: Austin, Dallas Ft-Worth, Denver, Los Angeles-Orange County, and the Inland Empire (Riverside/San Bernardino counties).

In summary, Opendoor's relatively large foot print provides the firm with a competitive advantage and first-mover status. However,the competitive field is very growing rapidly. For example, the CEO of Keller Williams' (a traditional realtor company) recently announced his company's intent to launch an iBuyer platform to respond to the challenge from this disruptive technology.    

---
## Business Results
The following table summarizes provides a high level summary of the rapid growth in Opendoor's operations. 

|Year   |Homes Sold      |Revenue        |Adj. EBITDA Margin |  Adj. EBITDA |    
|-------|:--------------:|:-------------:|:-----------------:|:------------:|
|2017   |     3,127      |     $0.7 B    |      <8.0%>       |    <$57 M>   |
|2018   |     7,470      |     $1.8 B    |      <7.1%>       |   <$131 M>   |
|2019   |    18,799      |     $4.7 B    |      <4.6%>       |   <$218 M>   |
|2020E  |     9,673      |     $2.5 B    |      <5.7%>       |   <$141 M>   |
---

The impact from COVID-19 is evident in 2020 as business operations were significantly disrupted in the second quarter. Opendoor reduced its staff by 35% in response to the sudden decline in business. As of June 2020, market sales were increasing and Opendoor, as well as it competitors, re-commenced buying homes. Operations have since resumed and services addressing customer concerns are being expanded.

The table below reflects Opendoor's projections for the full year 2020 through 2023.  As the company continues to expand its marketshare, it is able convert into more homes sold, increase revenues and improve its operating profit margin.

|Year   |Homes Sold      |Revenue        |Adj. EBITDA Margin |  Adj. EBITDA |    
|-------|:--------------:|:-------------:|:-----------------:|:------------:|
|2020E  |     9,673      |     $2.5 B    |      <5.7%>       |   <$141 M>   |
|2021P  |    13,458      |     $3.5 B    |      <5.4%>       |   <$185 M>   |
|2022P  |    24,030      |     $6.2 B    |      <2.0%>       |   <$123 M>   |
|2023P  |    37,689      |     $9.8 B    |      <0.1%>       |    $  9 M    |
---

### Long Term Growth Plan
Opendoor's growth plans include the following objectives:
* Expand from 21 markets to 100 markets by 2025.
* Increase marketshare from 2% to 4% in all markets the company operates.
* Seek to expand revenue sources and increase gross revenues to $50 billion.
* Continue to improve profitability by controlling operational costs and leveraging the firm's technology platform.

---
## Recommendations
The following list of recommendations are areas in which can further distinguish itself from the traditional realtor model as well as the growing presence of iBuyer competitors:
1. Focus on reputation of the firm. Continue building the brand and the company's image to existing and new customers. 
2. Continue to explore new sources of revenues in becoming a one-stop shop, but beware of low margin business, if possible. Continue to control costs to improve profitability.
3. Expand into new markets when it makes sense.  Make sure to keep investing in technology in order to be able to further scale up operations.  Try to maintain discipline and develop risk models to limit exposure in economically volatile markets. 
4.  An unfortunate drawback from becoming a public company is the ongoing and never ending reporting requirements.  This tends to add overhead costs and increasing the firm's breakeven threshold.  Management must continue to seek ways to control these costs and explore methods and ways to meet these burdens. 
5. An increased organizational size will exert pressure on talent acquisition. With growing competition in the iBuyer space, talent will likely become more difficult to secure at favorable wages.  

---
## Appendix
### Sources
1. Opendoor website - http://opendoor.com/
2. Opendoor Investor Presentation 
3. Forbes FinTech 50 Report (2019 and 2020 editions)
4. RedFin Q2 2020 iBuyer Report
5. Crunchbase - http://www.crunchbase.com/
6. Wikipedia - http://www.wikipedia.org/
7. Yahoo Finance - finance.yahoo.com
8. Linked In - http://linkedin.com/
9. National Association of Realtors -http://wwww.nar.com/
9. Stackshare - The Stack that helped Opendoor Buy and Sell over $1B in Homes (Blog) 
10. Curbed - The Real Estate Transaction is broken. Tech companies want to fix it (March 21, 2019)
11. BusinessWire - Opendoor, a Leading Digital Platform for Residential Real Estate Announces Plan to Become Publicly-traded via Merger with Social Capital Hedosophia (September 15, 2020)
12. HW+ - RedFinNow resumes in four more markets (June 26, 2020)
13. RedFinNow website - http://redfin.com/
14. Clever Real Estate - RedFinNow: How it works and what seller need to know (March 24, 2020)
15. Offerpad website - http://www.offerpad.com/
16. Zillow website - http://www.zillow.com/
17. Knock website - http://www.knock.com/
18. HW+ - Zillow offers resums buying in five more markets (May 27,2020)
19. Statista website - http://www.statista.com/



