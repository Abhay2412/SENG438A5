**SENG 438- Software Testing, Reliability, and Quality**

**Lab. Report \#5 – Software Reliability Assessment**

| Group \#21:       |   |
|-----------------|---|
| Student Names:  | Lauraine Baffot  |
|                 | Alexis Hamrak  |
|                 | Abhay Kholsa  |
|                 | Rachel Renegado  |

# Introduction
The main purpose of this lab was to help us discover the reliability assessment and the usage of the tools such as C-SFRAT and the Reliability Demonstration Chart with the help of Excel. This lab assignment also explored the failure reliability growth testing which helps analyze the product’s changes over a period of time. Additionally, this lab also introduced to us the concept of failure data which is critical to analyze as it can aid us in determining how to prevent future failures. Overall, these new concepts solidified the theoretical lectures helped us understand where reliability testing plays its role in software testing procedures. 
# 

# Assessment Using Reliability Growth Testing 
### Result of model comparison (selecting top two models)
In this section of the lab assignment, we had to select the best two models using the failure data provided to us the benefit of using the C-SFRAT was that we could simply import the CSV file into this GUI and we could use the functions to determine which fits in well with our data, this feature of Model Results and Predictions it will enable us to narrow which function resembles the closest to the failure data. To approach finding the best two models we select all the possible comparisons we could perform with the covariates. Here we can see all of the models which were selected to see which one would fit the best into our failure data. 

![](./Screenshots/All Models.png)

# Result of range analysis (an explanation of which part of the data is good for proceeding with the analysis)
For the range analysis, we had to look at the data which would fit the points on the failure data graph the best this was our strategy to achieve the best models from the ones the C-SFRAT provided to us. As mentioned above, we also made sure to look at the log-likelihood column and find the biggest two numbers (-57.100 and -59.147) and that is how we were able to identify our two top models displayed below. The range was also primarily used as the number of failures in the dataset as well in which we could create the 31 intervals to provide us analyzing our reliability of the failures which occurred during that time. 
# Plots for failure rate and reliability of the SUT for the test data provided	

# A discussion on decision making given a target failure rate	
For deciding on the failure rate target we used the C-SFRAT tool again to help us predict the testing of the new prediction intervals, we also used the other tool SRTAT to help with predicting the failure rate based on the failure number of the data. From both of these tools, we were able to make a target the failure rate being which is dividing the failure numbers by the total number of hours the system is running. Failure rate also helps us in determining how much we need to improve our testing in order to bring this rate down in order to gain assurance on the number of failures the system would experience when released to the end-users. Our aim was to have the lowest possible rate we could to ensure the reliability of the failure data given to us is not at a dangerous level in terms of the safety of the application. With our two predictions, we wanted to set a target of the failure rate to be 0.4 as this was the lowest intensity for both of the models in the desired intervals for the intensity graph displayed in the above section. With this target failure rate, the failure data shall provide reliability to the system under the testing where this data originated from. 
# A discussion on the advantages and disadvantages of reliability growth analysis

# Assessment Using Reliability Demonstration Chart 
## 3 plots for MTTFmin, twice and half of it for your test data
### MTTFmin 
![](./media/MTTFmin.png)
The above image displays the plot for MTTFmin. Through trial and error, we developed the plot above using the provided failure data as input to visualize the reliability of the system. As plotted, the reliability trend displayed suggests that the trend is acceptable for our FIO (does not dive heavily in the reject range). The calculation for MTTF, in this case, is 100/200,000, which gives an MTTF of 0.0005. 

### Half MTTFmin
![](./media/HalfMTTFmin.png)

The above image displays the plot for half MTTF. After the MTTFmin plot was found, the parameters were adjusted accordingly for half of the previous MTTF. The calculation for MTTF, in this case, is 25/100,000, which gives an MTTF of 0.00025. This trend dives more within the reject range which corresponds to the changes we made for this graph. Since we __decreased__ the number of acceptable failures, our failures in the half MTTF plot should have more data points in the __reject__ region. 

### Twice MTTFmin
![](./media/TwiceMTTFmin.png)

The above image displays the plot for twice MTTF. After the MTTFmin plot was found, the parameters were adjusted accordingly for twice of the initial MTTF. The calculation for MTTF in this case is 400/400,000, which gives an MTTF of 0.001. This trend dives more within the acceptable range which corresponds to the changes we made for this graph. Since we __increased__ the number of acceptable failures, our failures in the twice MTTF plot should have more data points in the __accept__ region.

## A discussion on the advantages and disadvantages of RDC
### Advantages
- RDC is a fairly simple way to assess a system’s reliability. It is very straightforward to assemble a spreadsheet or find a tool to plot test data with and determine how the SUT performs over time. In addition, it does not require much time to generate the plots and analyze them. 
- RDC is a very low-cost method of determining system reliability because the software required to generate the plots is nothing fancy, just a simple excel sheet will work.
### Disadvantages
- RDC is unable to output a quantitative number for the reliability of a system. A reliability number would be important and very useful in support of decisions and making conclusions on the overall reliability of the system. Unfortunately, RDC is unable to develop this quantitative value but can only visualize the trend for reliability.
- The MTTF needs to be calculated and unfortunately, it requires a lot of “guess and check” to see which value works the best. This requires rather tedious amounts of work if you do not have an idea of what value to use.

# Comparison of Results

# Discussion on Similarity and Differences of the Two Techniques

# How the teamwork/effort was divided and managed
The team decided to work all together for this lab. We first installed the tools that were required to complete the lab and worked together to understand how the tools worked. We decided to use C-SFRAT because it seemed to work the best with our laptops. Unfortunately, Alexis and Rachel were unable to use the tool on their computers, so in order to split the work evenly, Abhay and Lauraine worked on Part 1 using C-SFRAT and SRTAT, and Alexis and Rachel worked on Part 2 with the RDC excel chart. After all of the necessary components such as failure ranges were compiled and the graphs were finished, all of the members worked together to write the report and discuss how their tools worked and what their results were.

# Difficulties encountered, challenges overcome, and lessons learned
There were obstacles that resulted from the incompatibilities with Mac OS and the software that were required to complete the lab. Due to this incompatibility, it was difficult to work efficiently when only half the group was able to operate the appropriate software (C-SFRAT) to visualize and analyze the data. We overcame this challenge by implementing a peer programming style approach to this lab by having the two working computers use C-SFRAT and the other two analyze the data visuals generated. 

# Comments/feedback on the lab itself
In the future, it would be more efficient and beneficial to all students if the software used in the lab was compatible with all OS to eliminate the obstacles we had to face.
