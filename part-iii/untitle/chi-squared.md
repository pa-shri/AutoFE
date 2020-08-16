# Chi-Squared

A chi-square test is used in statistics to test the independence of two events. Given the data of two variables, we can get observed count O and expected count E. Chi-Square measures how expected count E and observed count O deviates each other.

                                                ![Image for post](https://miro.medium.com/max/532/1*S8rfFkmLhDbOz4RGNwuz6g.png)

Let’s consider a scenario where we need to determine the relationship between the independent category feature \(predictor\) and dependent category feature\(response\). In feature selection, we aim to select the features which are highly dependent on the response.

When two features are independent, the observed count is close to the expected count, thus we will have a smaller Chi-Square value. So high Chi-Square value indicates that the hypothesis of independence is incorrect. In simple words, the higher the Chi-Square value the feature is more dependent on the response and it can be selected for model training.

Steps for Chi-Square Test with an example:

Consider a data-set where we have to determine why customers are leaving the bank, let’s perform a Chi-Square test for two variables. _**Gender**_ of a customer with values as Male/Female as the predictor and _**Exited**_ describes whether a customer is leaving the bank with values Yes/No as the response. In this test we will check _is there any relationship between Gender and Exited_.

Steps to perform the Chi-Square Test:

1. Define Hypothesis.
2. Build a Contingency table.
3. Find the expected values.
4. Calculate the Chi-Square statistic.
5. Accept or Reject the Null Hypothesis.

### 1.Define Hypothesis <a id="5ef5"></a>

Null Hypothesis \(H0\): Two variables are independent.

Alternate Hypothesis \(H1\): Two variables are not independent.

### 2. Contingency table <a id="5ca2"></a>

A table showing the distribution of one variable in rows and another in columns. It is used to study the relation between two variables.

                                     ![Image for post](https://miro.medium.com/max/834/1*rmQj1uMkdvIISYaUa6rzgg.png)

Contingency table for observed values

Degrees of freedom for contingency table is given as \(r-1\) \* \(c-1\) where r,c are rows and columns. Here df = \(2–1\) \* \(2–1\) = 1.

In the above table we have figured out all observed values and our next steps are to find expected values, get the Chi-Square value and check for relationship.

### 3. Find the Expected Value <a id="1d51"></a>

Based on the null hypothesis that the two variables are independent. We can say if A, B are two independent events

                                            ![Image for post](https://miro.medium.com/max/414/1*sD5qNUh_lsiXjSF_dE6W_g.png)

Let’s calculate the expected value for the first cell that is those who are Males and are Exited from the bank.

                                            ![Image for post](https://miro.medium.com/max/552/1*QpKU8h5I9jAwaVavmX0J5g.png)                                                 

The calculation for the expected value

In similar, way, we calculate E2, E3, E4 and get the following results.

![Image for post](https://miro.medium.com/max/862/1*yvWLhvZNS5_CvX5st6Bylg.png)

Expected values

### 4. Calculate Chi-Square value <a id="2384"></a>

Summarizing the observed values and calculated expected values into a table and determine the Chi-Square value.

![Image for post](https://miro.medium.com/max/1020/1*pScat3UxYpoGeKCdm3-_pQ.png)

            ![Image for post](https://miro.medium.com/max/510/1*FV8dmB9BgkFOLai2WlqTeA.png)

We can see Chi-Square is calculated as 2.22 by using the Chi-Square statistic formula.

### 5. Accept or Reject the Null Hypothesis <a id="1468"></a>

With 95% confidence that is alpha = 0.05, we will check the calculated Chi-Square value falls in the acceptance or rejection region.

Having degrees of freedom =1\(calculated with contingency table\) and alpha =0.05 the Chi-Square value is 3.84.

The Chi-Square values can be determined with the [Chi-Square table](https://web.ma.utexas.edu/users/davis/375/popecol/tables/chisq.html).

\_\_

