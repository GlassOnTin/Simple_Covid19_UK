# A Simple Covid-19 compartmental model for the United Kingdom
A simple (naive, empirical, student, amateur) [compartmental epidemiological model](https://en.wikipedia.org/wiki/Compartmental_models_in_epidemiology) of the Covid-19 outbreak in the United Kingdom, using the Microsoft Excel solver to optimise the parameters.

This model partitions the United Kingdom population into three situations:
* Susceptible - those who are prone to infection with Covid-19;
* Infected - those who are currently infected and contagious;
* Recovered / deceased - those who have had the virus.

The model is fitted to data collated from the [2020 coronavirus pandemic in the United Kingdom](https://en.wikipedia.org/wiki/2020_coronavirus_pandemic_in_the_United_Kingdom) wiki page.

The model fits the following parameters for discrete periods of lockdown / free movement:
* Reproductive rate, R(t) = 2.7 before lockdown, 1.3 after lockdown;
* Case fatality rate, CFR(t) = 2% of confirmed cases;
* Proportion of cases that are symptomatic, _tested and test positive for COVID-19_ = 3% to 1.5%;
* Recovery rate (gamma) - 4 days to recover;
* Hospitalisation rate of infected cases - 2%

The proportion of cases that are symptomatic, tested and test positive parameter is the most critical piece of information to judge the best strategy to lift the lockdown.  This parameter wraps-up both the testing rate _and_ the proportion of symptomatic cases together.  Once the position of the peak was known, there was enough information to fit this parameter.

The hospitalisation rate of positively tested cases is calculated by fixing the maximum hospitalisation level to 25,000 based on Office for National Statistics data.

A scenario is modelled where the lockdown of April 2020 is continued until August 2020.  The model results indicate 35% of the population are immune by August and the positive test rates will have dropped to 50 per day and 250 Covid-19 patients will still be in hospital. Lifting the lockdown for the month of August takes the hospitalised cases back up to 1,400 cases and causes a further 800 hospitalised deaths.   Reintroducing full lockdown again in September gets the hospitalisation back down again.  The real test is how fast the infection rate picks up again when lock-down is lifted.

## Charts assuming lockdown is lifted in August 2020
![Hospitalisation](Hospitalised.png?raw=true "Hospitalisation")
![Immune](Immune.png?raw=true "Immune")
![Positive Test Rate](PositiveTestRate.png?raw=true "Positive Test Rate")
![Fatality Rate](FatalityRate.png?raw=true "Fatality Rate")
![Deceased](Deceased.png?raw=true "Deceased")
![Infected](Infected.png?raw=true "Infected")


