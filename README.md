Download Link: https://assignmentchef.com/product/solved-buan6356-assignment2
<br>
<ol>

 <li>Create an R Markdown document to prepare your answers. You should upload <strong>two (2)</strong> files on eLearning: (i) an <strong>.RMD</strong> file; and (ii) a <strong>.PDF</strong> file that is generated using “knit” in the .RMD file.  Both files should contain the required R code, R tables and charts, and all the required explanations and answers to the questions in the homework.</li>

 <li>Write your answers outside of the code chunks in the R markdown file (rather than using comments inside code chunks).</li>

 <li>Include your name and netID at the top of the file.</li>

 <li><strong>DO NOT</strong> use an absolute directory path. I should be able to “knit” your R Markdown document to an .html/.pdf document without trying to find the input data in another directory.  Test the “knit” process before uploading files on eLearning.  Assume that I have the .csv file(s) mentioned below.</li>

 <li><strong>DO NOT</strong> change the dataset name before importing it into R. If you rename the dataset or any variable(s), use your R script to do that.</li>

 <li>Use <em>seed(42)</em> anywhere you need to set a seed.</li>

 <li>Label the charts and/or tables appropriately. Your reader should be able to figure out what information a chart is providing by looking at the chart title and its labels.</li>

 <li>Any assignment submitted after the deadline will be considered late and will not be graded.</li>

</ol>

<h1><u>Homework 2</u></h1>

A consulting firm working for Southwest Airlines would like to predict airfares using

<strong><em>Airfares.csv</em></strong>, which contains real data that were collected between Q3-1996 and Q2-

<ol start="1997">

 <li>The variables in these data are listed below. Some airport-to-airport data (<em>e.g.,</em> JFK-BWI) are available, but most data are at the city-to-city level (<em>e.g.,</em> Atlanta-Boston).  A key question is whether the presence or absence of Southwest Airlines (a low-cost entrant) would have any effect on <em>fare</em>.</li>

</ol>




<strong><em>Variable Description: </em></strong>

S_CODE:  Starting airport’s code

S_CITY:  Starting city

E_CODE:  Ending airport’s code

E_CITY: Ending city

COUPON:  Average number of coupons for that route  <em>(a one-coupon flight is a nonstop flight, a two-coupon flight is a one-stop flight, etc.) </em>

NEW:  Number of new carriers entering that route between Q3-96 and Q2-97

VACATION:  Whether (Yes) or not (No) a vacation route

SW:  Whether (Yes) or not (No) Southwest Airlines serves that route

HI:  Herfindahl index, a measure of market concentration  <em>(higher number means smaller number of available carriers on that route) </em>

S_INCOME:  Starting city’s average personal income

E_INCOME:  Ending city’s average personal income

S_POP:  Starting city’s population

E_POP:  Ending city’s population

SLOT:  Whether or not either endpoint airport is slot-controlled <em>(this is a measure of airport congestion) </em>

GATE:  Whether or not either endpoint airport has gate constraints <em>(this is another measure of airport congestion) </em>

DISTANCE:  Distance between two endpoint airports in miles

PAX:  Number of passengers on that route during period of data collection

FARE:  Average fare on that route




Remove the first four predictors (S_CODE, S_CITY, E_CODE, E_CITY) from all your analysis below.

<ol>

 <li>Create a correlation table and scatterplots between FARE and the predictors. What seems to be the best single predictor of FARE? Explain your answer.</li>

</ol>




<ol start="2">

 <li>Explore the categorical predictors by computing the percentage of flights in each category. Create a pivot table with the average fare in each category.  Which categorical predictor seems best for predicting FARE?  Explain your answer.</li>

</ol>




<ol start="3">

 <li>Create data partition by assigning 80% of the records to the training dataset. Use rounding if 80% of the index generates a fraction.  Also, set the seed at <em>42</em>.</li>

</ol>




<ol start="4">

 <li>Using <em>leaps</em> package, run stepwise regression to reduce the number of predictors. Discuss the results from this model.</li>

</ol>




<ol start="5">

 <li>Repeat the process in (4) using exhaustive search instead of stepwise regression. Compare the resulting best model to the one you obtained in (4) in terms of the predictors included in the final model.</li>

</ol>




<ol start="6">

 <li>Compare the predictive accuracy of both models—stepwise regression and exhaustive search—using measures such as RMSE.</li>

</ol>




<ol start="7">

 <li>Using the exhaustive search model, predict the average fare on a route with the following characteristics: COUPON = 1.202, NEW = 3, VACATION = No, SW = No, HI = 4442.141, S_INCOME = $28,760, E_INCOME = $27,664, S_POP = 4,557,004, E_POP = 3,195,503, SLOT = Free, GATE = Free, PAX = 12,782, DISTANCE = 1976 miles.</li>

</ol>




<ol start="8">

 <li>Predict the reduction in average fare on the route in question (7.), if Southwest decides to cover this route [using the exhaustive search model above].</li>

</ol>




<ol start="9">

 <li>Using <em>leaps</em> package, run backward selection regression to reduce the number of predictors. Discuss the results from this model.</li>

</ol>




<ol start="10">

 <li>Now run a backward selection model using <em>stepAIC()</em> Discuss the results from this model, including the role of AIC in this model.</li>

</ol>





