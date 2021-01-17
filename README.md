![Respondants per country](https://github.com/lhache/lgbt-data/blob/main/images/eu-lgbt.jpg?raw=true)

# LGBT discrimination in the EU - intuition vs analysis

## The survey

The survey details can be read [here](https://fra.europa.eu/sites/default/files/eu-lgbt-survey-technical-report_en.pdf).
This survey has been conducted throughout the EU (and Croatia) by the [FRA](https://europa.eu/european-union/about-eu/agencies/fra_en) (European Union Agency for Fundamental Rights).

## A quick look at the data

The total amount of respondants is 93 079.

The survey posseses 5 datasets, around the topics of discrimination, rights awareness, daily life and violence & harassment.

Where do the respondants come from?

![Respondants per country](https://github.com/lhache/lgbt-data/blob/main/images/respondants-per-country.png?raw=true)

In which subset do they fall into?

![Respondants per category](https://github.com/lhache/lgbt-data/blob/main/images/respondants-per-category.png?raw=true)


## Methodology

The goal was to create a discrimination score from the given answers. From this score, we can compare discrimination within countries or subsets.

In the case of this analysis, only the discrimination dataset was used. 
The responses were of 3 categories:
- free text
- yes/no/don't know
- very rare/rare/often/very often/don't know
Only the yes/no questions were selected, excluding the others.

1. normalising percentages
Each answer is given with a percentage but we cannot use them as is because the ratio of Lesbians/Gays/Bisexuals/Transgenders is normal equal within the countries. Therefore, the percentages have been normalised with the weight of each subset.

2. setting a score for yes/no/don't know answers
In order to create the discrimination score, each answer type was given a score.
- Don't know answers were given N/A and were dropped from the analysis
- Yes was given -1 (because pointing to more discrimination)
- No was given 1

3. setting the discrimation score
The answer score and the weighted percentages were combined to give the discrimination score.


## Question 1: do LGBT people feel less discriminated in Germany compared to France?

I am french but I'm living in Berlin since 8 years. My gut feeling says there's more acceptance towards LGBT people in Germany than in France but I would like to go through the data and look at what we can find out regarding this question.
I also have to take personal biases into account. I was born and grew up in a very small village in south of France, which is not quite representative of the whole french population. Similarly for Germany, I've only lived in Berlin which seems much more LGBT-friendly that many other places, including the rest of Germany. All in all, one bubble versus another.

So let's see what we can see from the data:

![Scores per subset](https://github.com/lhache/lgbt-data/blob/main/images/scores-per-country.png?raw=true)

*Conclusion*
The data seem to indicate there is not much real difference between France and Germany.


## Question 2: is there a diagonal in Europe?

I've got to travel quite a bit and have had the chance to meet people from many many different countries. I'd say that Scandinavia and western Europe tend to be acceptive towards LGBT, while eastern Europe would be on the other side of the spectrum.

![My mental diagonal](https://github.com/lhache/lgbt-data/blob/main/images/eu-diagonal.png?raw=true)

Let's compare with the results from the analysis. The higher the score, the less reported discrimination.

![Map from analysis results](https://github.com/lhache/lgbt-data/blob/main/images/map-output.png?raw=true)

*What can we infer from that?*
- it seems there is more discrimination in eastern and southern Europe but it's not a standard.
- The UK case is quite puzzling, I'm wondering whether this is anomaly or not.


## Question 3: do transgenders feel more discriminated than other categories?

My gut feeling is that there is more discrimination towards transgenders than towards homosexuals or bisexuals.

Let's look again at the scores from the analysis:

![Scores per subset](https://github.com/lhache/lgbt-data/blob/main/images/scores-per-category.png?raw=true)

*Conclusion*
The data seems to indicate that yes, transgenders seem to be/feel more discriminated than the other members of the LGBT people. 


## Improvements on the analysis

A few things could have been made better, such as:
- use the entire discrimination dataset instead of a subset of it
- use all the four other datasets because they also relate to discrimination questions

