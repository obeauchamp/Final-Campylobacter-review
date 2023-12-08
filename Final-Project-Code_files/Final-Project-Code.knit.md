---
title: 'Final Assignment Analysis: Epidemiological Review of Campylobacteriosis in
  the European Union'
author: "Olivia Beauchamp"
date: "2023-12-08"
output:
  pdf_document: default
  html_document: default
  word_document: default
---

Git Hub Repository Link <https://github.com/obeauchamp/Final-Campylobacter-review.git>

### Introduction

The interactions between animals and humans within the environent significantly contribute to the emergence and transmission of infectious diseases. Driven by a complex variety of factors such as land use changes, consumption of animal products and agricultural practices, international travel, understanding the ability of pathogens to expand and adapt to new niches is vital to ensure the safety of global public health (Ferreira, 2021). In this study, data from the European Centers of Disease Control will be used to observe the prevalence and temporal patterns in zoonotic infections in the European Union. Particular attention will be drawn on Campylobacter, the most frequently reported pathogen in the European Union since 2005.

### Methods

*Generating data frames*

Data was sourced from the European Union Summary Report on Trends and Sources of Zoonoses and the Surveillance Atlas of Infectious Diseases. The data was cleaned and structured to long format using gather from the forcats package. Summarize and mutate from dpylr was then used. generate percent distributions for individual data frames.









*Visualization and Data Analysis*

The 2021 Summary provided an snapshot of the most recent incidents of zoonotic diseases (EU 2021). A data frame containing cases for 2021 was generate and rearranged in descending order of cases. A pie chart to illustrate the distrubution of cases by disease was constructed in ggplot (Fig 1). The corresponding table was generated with ddpylr.

Due to the high abundance of Campylobacter and Salmonella in 2021, the temporal patterns of these diseases as well as other recorded zoonotic diseases was examined. Given how the disparity between case counts did not allow for close examination of the prevalence over time when taken together, each diseases was arbitrarily categorized and sorted into a separate data frame by prevalence. Diseases with high case counts accounted for more than 10,000 cases each year and diseases with a moderate prevalence accounted between 10,000-500 cases yearly. Finally, less infrequent diseases, were sorted based on if they accounted for less than 1,000 cases yearly. ggplot was used then to plot the prevalence of each over the reported period accordingly (Fig 2).

In 2020, the amount of cases significantly dropped for the most frequently reported diseases, Campylobacter and Salmonella, and coincidentially, the total cases overall also decreased with the departure of the UK from the European Union. To see if any other country significantly contributed to the total cases of Campylobacter, case counts were graphed using ggplot (Fig 3). The percent distribution of Campylobacter cases by country is also displayed (Table 2). At this point, attention will be focused on Campylobacter, as it was the most prevalent disease in the EU since 2005.

Finally, two data frames were created to observe gender distribution of Campylobacter. First, the percent of cases reported among men and women in each country in 2021 was created and plotted in ggplot (Fig 4). To determine if there was a bias towards men throughout the study period, a data frame containing the percent gender distribution from 2021-2011 was constructed and plotted using ggplot (Fig 5). To further solidify the association of cases of men being more frequently reported linear regression model was performed on the overall gender distribution in cases.

### Results



![](Final-Project-Code_files/figure-latex/unnamed-chunk-6-1.pdf)<!-- --> 
In 2021, Campylobacter and Salmonella accounted for an overwhelmingly majority of reported cases, overshadowing the incidence rates of all other reported illnesses combined (Figure 1).

Campylobacteriosis, caused by the bacteria Campylobacter was confirmed as the most commonly reported disease in the EU. In 2021 it accounted for 127,840 cases with a prevalence of 62.3% overall. Salmonella was also frequently reported and accounted for 60,050 cases with a prevalence of 29%. Yersiniosis, Shiga Toxin-producing E.coli (STEC infections), and Listeriosis, illnesses associated with eating raw or under cooked meat were less frequently reported. Diseases such as for Q-fever, West Nile Virus, and Rabies, in which humans are dead-end hosts, were reflected in their relatively low percent abundance.



![](Final-Project-Code_files/figure-latex/unnamed-chunk-8-1.pdf)<!-- --> ![](Final-Project-Code_files/figure-latex/unnamed-chunk-8-2.pdf)<!-- --> ![](Final-Project-Code_files/figure-latex/unnamed-chunk-8-3.pdf)<!-- --> 
In order to assess the trends of human infections in the European Union, case counts for each zoonosis from 2005 to 2021 was plotted and displayed in Figure 2.

In the European Union, Campylobacter consistently showed the highest number of cases since 2005, with a noticeably higher prevalence than all other diseases with animal origins. Over the 17-year study period, Campylobacter accounted for 3,476,055 cases, with an overall abundance of 23.44%. Routes of transmission of this pathogen include consumption of contaminated food and water, contact with animals, and transmission between infected individuals (Facciolà A, 2017). Salmonella, another pathogen associated with eating contaminated food, reported significantly high case counts over the study period, accounting for 1,753,462 total cases with a prevalence of 11.82% overall. Because the source of these infections are linked to food, it was not suggested how the prevalence and associations to food-borne outbreaks vary over time.

In general, the incidence of Listeriosis, STEC infections and Yersiniosis varied slighty throughout the study period. Shiga Toxin E.coli infected 2,500-8,000 individuals yearly, Listeriosis infected 2,000-3,000 individuals yearly, with a moderate overall increase starting in 2014, and Yersiniosis cases varied between 5-10,000 cases yearly, except in 2012, where no cases were reported. For less frequently reported diseases, the prevalence each varied drastically.



![](Final-Project-Code_files/figure-latex/unnamed-chunk-10-1.pdf)<!-- --> 
Given the high prevalence of Campylobacter throughout the study period, cases from each country were plotted to determine if the prevalence could be identified to a specific region, or if it was evenly distributed across Europe (Fig 3).

As reported in Figure 3, the majority of cases in 2021 were attributed to Germany, accounting for 47,911 infections, or 33.9% of all cases reported. Following Germany, Spain, Czechia, France, Slovakia, Austria, Belgium, and Sweden reported more than 5,000 cases in 2021 with a prevalence of 14.7%, 11.5%, 6.3%, 4.3%, 4.2%, 3.6%, and 2.9% respectively. Despite a third of cases being associated with Germany, the widespread distribution of the disease suggests that Campylobacter is not limited to any one country in particular.

![](Final-Project-Code_files/figure-latex/unnamed-chunk-11-1.pdf)<!-- --> 
While sourcing data from the EU Surveillance Atlas of Infectious Diseases, it was noticed that Campylobacter was more frequently reported in men than in woman, as highlighted in figure 4.



![](Final-Project-Code_files/figure-latex/unnamed-chunk-13-1.pdf)<!-- --> 
In every country except for Bulgaria, Iceland, and the Netherlands, men represented the majority of cases. Given this association, the gender distribution of all cases in 2021-2011 was graphed to investigate if this trend was consistent over a longer study period (Fig 5).

As shown in Figure 5, the disparity in the gender distribution of Campylobacter has occured over at least a 10 year study period. Since 2011, more cases were reported in men than in woman, which has widened throughout time. Linear regression analysis of the data found a moderately positive association between the incidence of men being infected, with a correlation coefficient of 0.463. The R-squared value of 0.9678 indicates that approximately 96.78% of the variance in the cases is due to gender, suggesting the model fits the data. Taken together, this suggests that men in the EU are more likely to be infected with Campylobacter.

### **Discussion**

This study examined the prevalence of zoonotic infections in the European Union. Overall, Campylobacter was overwhelmingly the most frequently reported pathogen since 2005, infecting over 100,000 individuals yearly.

In examining the temporal patterns of zoonotic diseases, it is noted that the withdrawal of the UK from the European Union in early 2020 resulted with a decrease in the prevalence of all diseases, except Echinococcosis, Brucellosis, and Tuberculosis. Of particular importance, the most highly reported zoonotic pathogens, Campylobacteriosis and Salmonellosis are among the most common causes of food poisoning in the UK (EU CDC). The impact of COVID-19 was also evident in reduced cases of all zoonotic infections from 2019 to 2020. With an increased public awareness of hygiene and food handling practices, as well as limited exposure to environmental sources of infection, it is likely that the decline in reported cases reflected a genuine reduction in disease prevalence. However, it is still worth noting that the decline infections are likely contributed to the challenges people sought while seeking medical attention for non-COVID-19 related illnesses, and that the case counts in 2020 do not reflect the true prevalence of these pathogens.

To further understand how Campylobacter cases were distributed throughout the EU, this report found that a third of cases were reported in Germany with a tendency to infect men more often than women. A 10-year epidemiological study on the prevalence of *Campylobacter* in Germany found that 97% of cases were reported as sporadic, meaning they were not associated with an outbreak. They additionally associated 8% of cases in Germany as travel-related to Spain, Turkey, France, Italy, and India, several countries in the European Union with relatively higher case counts (Schielke et al, 2014). While not highlighted in this study, the reasons behind the sexual dimorphism of this bacterium are being elaborated upon within the scientific community (Green, 2020 and Strachan, 2008).

#### Citations

Rahman MT, Sobur MA, Islam MS, Ievy S, Hossain MJ, El Zowalaty ME, Rahman AT, Ashour HM. Zoonotic Diseases: Etiology, Impact, and Control. Microorganisms. 2020 Sep 12;8(9):1405. doi: 10.3390/microorganisms8091405. PMID: 32932606; PMCID: PMC7563794.

Ferreira, Mariana & Ellio, Wendy & Golden Kroner, Rachel & Kinnaird, Margaret & Prist, Paula & Valdujo, Paula & Vale, Mariana. (2021). Drivers and causes of zoonotic diseases: An overview. PARKS. 27. 15-24. 10.2305/IUCN.CH.2021.PARKS-27-SIMNF.en.

European Centers of Disease Control and Prevention. Surveillance and disease data on food and water-borne diseases and zoonoses (2021-2011). *EFSA Journal*, <https://www.ecdc.europa.eu/en/food-and-waterborne-diseases-and-zoonoses/surveillance-and-disease-data>

Facciolà A, Riso R, Avventuroso E, Visalli G, Delia SA, Laganà P. *Campylobacter:* from microbiology to prevention. J Prev Med Hyg. 2017 Jun;58(2):E79-E92. PMID: 28900347; PMCID: PMC5584092.

Schielke A, Rosner BM, Stark K. Epidemiology of campylobacteriosis in Germany - insights from 10 years of surveillance. BMC Infect Dis. 2014 Jan 15;14:30. doi: 10.1186/1471-2334-14-30. PMID: 24422983; PMCID: PMC3898467.

Green, M.S., Schwartz, N. & Peer, V. Sex differences in campylobacteriosis incidence rates at different ages - a seven country, multi-year, meta-analysis. A potential mechanism for the infection. *BMC Infect Dis* **20**, 625 (2020). <https://doi.org/10.1186/s12879-020-05351-6>

Strachan NJ, Watson RO, Novik V, Hofreuter D, Ogden ID, Galán JE. Sexual dimorphism in campylobacteriosis. Epidemiol Infect. 2008 Nov;136(11):1492-5. doi: 10.1017/S0950268807009934. Epub 2007 Dec 7. PMID: 18062834; PMCID: PMC2870750.).
