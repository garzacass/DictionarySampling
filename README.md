# DictionarySampling
Estimate of the percentage of words I know in the English and Spanish dictionaries using different statistical sampling methods in R

### Methods
To calculate this, we first estimate the total amount of words in the dictionary, as well as the amount of words I know from the dictionary in total. We divide the words I know by the total number of words, and multiply it by 100 to find the estimated percentage.
We explore four different sampling methods for each language: simple random sampling, stratified sampling with proportional allocation, cluster sampling, and systematic sampling. We calculate the desired values, along with their standard error. I will briefly walk through the steps that have to be taken for each sampling method:
Simple random sampling is the simplest of the four. We simply generate a random 45 pages to sample, then collect our data. After that, we create our design and make the necessary calculations. Next is Stratified sampling. For this method, I chose to stratify by letter of the alphabet. Having our stratum, we then proportionally allocate the 45 samples we want for each stratum. We also calculate our fpc, then we can create our design and make the necessary calculations. Next, is cluster sampling. For this method, we cluster by letter of the alphabet. Then, we calculate the amount of clusters we need to sample based on the average number of pages per cluster and randomly select (45average) clusters, and create our design and make necessary calculations. The last sampling method is systematic sampling. For this method, we calculate k (k=Nn) and take every kth sample from the dictionary pages. We also calculate the weight of each sample, then create our survey design and make the necessary calculations.
To wrap up the results, I calculated the difference between the percentage I know for each language for each sampling method, as well as the confidence intervals for the calculations. I also created a bar graph with error bars to visually represent the percentages calculated.

### Results
The resulting estimated percentages and their confidence intervals are as follows. Based on the simple random sampling, I know 82.108% of the English dictionary with a confidence interval [-23.2, 187.4] and 82.015% of the Spanish dictionary with a confidence interval of [79.5, 84.5]. Based on stratified sampling, I know 83.242% of the English dictionary with a confidence interval [82.9, 83.6] and 83.971% of the Spanish dictionary with a confidence interval of [83.3, 84.7]. Based on cluster sampling, I know 79.896% of the English dictionary with a confidence interval [79.3, 80.5] and 84.403% of the Spanish dictionary with a confidence interval of [83.4, 85.4]. Lastly, based on systematic sampling, I know 81.343% of the English dictionary with a confidence interval [79.1, 83.6] and 83.793% of the Spanish dictionary with a confidence interval of [80.8, 86.8].

The difference in percentage estimates between English and Spanish knowledge is minimal (0.09%) with a bad confidence interval spanning from -105.21% all the way to 105.40%. This uncertainty is reflective of the variability introduced by the random sampling process. Stratified sampling has a difference of -0.73% between English and Spanish languages. This calculation has a relatively narrow confidence interval of [-1.11%, -0.35%]. This shows that taking strata into account helps reduce variability, providing a more precise estimate. Cluster sampling has the largest difference between the two languages: a difference of -4.51% between English and Spanish. The confidence interval for this is [-5.08%, -3.95%]. Lastly, systematic sampling indicated a -2.45% difference in my knowledge between English and Spanish. However, the confidence interval is a bit larger: [-4.67%, -0.22%].

### Conclusion
The results from all the different sampling methods provide valuable insights. The discrepancies in language knowledge estimates across different sampling methods provide valuable insights into the nuances of survey design. Something that’s important to note, is that the percentage of known words varies across the sampling methods, reflecting the impact of the sampling design on the estimation. Each sampling method offers unique advantages and disadvantages.

While the results for both languages using simple random and systematic sampling were similar, stratified sampling stands out as the method with the most precise estimate. This suggests that accounting for strata based on certain characteristics enhances the accuracy of estimates. This is possible because we are then able to reflect variations in language knowledge across different subgroups. 

In contrast, cluster sampling and simple random samples have larger confidence intervals, indicating a higher level of variability in the estimates. This variability could be influenced by the grouping of pages into clusters or the randomness of the sampling process. Systematic sampling may not consistently outperform other approaches in terms of precision, but it remains a viable choice for scenarios where simplicity and efficiency are important. One thing to note is that it seems to be limited when it comes to capturing variability.

These results emphasize the importance of selecting an appropriate sampling strategy based on the objectives and the characteristics of the population. The strategy we choose plays a large role in metrics such as accuracy and reliability. No single method is universally superior, but we tailor our approach to the characteristics of the population and the specific objectives of the study. The results make sense. My first language is Spanish and I grew up speaking English in school, so it’s not extremely unlikely for me to know about the same percentage of English and Spanish. Something that may have impacted them is also that the English one contains words from other origins such as French origin or British origin. However, the Spanish dictionary did not.


Here’s a quick visual representation of the percentages found across all samples:
<img width="469" alt="Screenshot 2024-01-30 at 9 35 43 AM" src="https://github.com/garzacass/DictionaryAnalysis/assets/91804805/833bac67-3987-42d0-a7d6-6942b05cabbd">

<img width="469" alt="Screenshot 2024-01-30 at 9 36 11 AM" src="https://github.com/garzacass/DictionaryAnalysis/assets/91804805/a8c77f35-d482-4143-9e11-4052f30590c6">







