##  ESG Scores in Latin American Markets 

**Introduction:** 
Latin America is an emergent focus for inversion and innovation. The idea that countries are still young tells that many things
are left to do and to exploit, making it an interesting point for economic growth. Although all this good inversions opportunities, 
Latin America is branded as an irregular market. The diverse problems like social outbreaks, corruption, government instability, environmental damage, etc;
give the investors less trust to put there money in Latin America stocks. But as it's say, the bigger the risk the bigger the reward. For this reason is vital to analyse all the companies under different scopes, being environmental, social and corporate governance (ESG) the most relevant ones. The goal of this project is make the analysis under this three aspects for more than 100 Latin American companies, see how they affect in there discount rate and relate on the return of a company or certain type of industry.

**Methods and Materials:**
This project requires knowledge in big data, financials and econometrics. 
To analyse the return of a company the discount rate has to be calculated. HOLT employs a total system approach to measuring and forecasting corporate returns (for more information see <a href="https://onlinelibrary.wiley.com/doi/10.1002/9781119440512.ch7">Beyond Earnings</a>). In this project the HOLT discount rate for every company is taken from _Credit Suisse_. 

All the code was implement in Python. 

**Development:**
ESG refers to the three central factors in measuring the sustainability and societal impact of an investment in a company or business.
These criteria help to better determine the future financial performance of companies, return and risk. We made a questionnaire of 101 multiple choice questions related to ESG and we make all the analysts to answer it for every company that trades in the stock market of Latin America. We determine a ESG score with the next equeation:

<img src="https://render.githubusercontent.com/render/math?math=ESG = x_1w_1 %2B x_2w_2 ... %2B x_iw_i ... %2B x_101w_101">

Where __x__ is the answer of the question i and __w__ is the weight of that question. The __x__ value is assigned depending on the answer and it takes values between 0 and 1. The weight will be calculated through an optimisation model that it will be explained later.
Making a simple assumption that for a high ESG score, the lower the HOLT will be. This in general is true, companies that have better behavior, the market will reward with a better revenue, or in other words, with a lower discount rate. The fucntion that explain this: 

<img src="https://render.githubusercontent.com/render/math?math=Y = \beta_0 %2B \beta_1ESG %2B \beta_2ESG^2 %2B \beta_3ESG^3">

**Results:**



**Conclusion:**
Nowadays people are very aware of what companies are doing, if they are frendly to the enviroment, or if the labor conditions are acceptable.


_(Agust, 2019) Compass Group Asset Management, Santiago, Chile. <br>
All the intellectual property of this project belongs to Compass Group Asset Management._
