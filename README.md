# A Simple Covid-19 compartmental model for the United Kingdom
A simple (naive, empirical, student, amateur) [compartmental epidemiological model](https://en.wikipedia.org/wiki/Compartmental_models_in_epidemiology) of the Covid-19 outbreak in the United Kingdom, using the Microsoft Excel solver to optimise the parameters.

This model partitions the United Kingdom population into three situations:
* Susceptible - those who are prone to infection with Covid-19;
* Infected - those who are currently infected and contagious;
* Recovered / deceased - those who have had the virus.

The model is fitted to data collated from the [2020 coronavirus pandemic in the United Kingdom](https://en.wikipedia.org/wiki/2020_coronavirus_pandemic_in_the_United_Kingdom) wiki page.

The model fits the following parameters for discrete periods of lockdown / free movement:
* Reproductive rate, R(t) = 2.0 before lockdown, 1.1 after lockdown;
* Case fatality rate, CFR(t) = 2% of confirmed cases;
* Proportion of cases that are symptomatic, _tested and test positive for COVID-19_ = 7% to 3%;
* Recovery rate (gamma) - 4 days to recover;
* Hospitalisation rate _of positively tested cases_ - 42%

The proportion of cases that are symptomatic, tested and test positive parameter is the most critical piece of information to judge the best strategy to lift the lockdown.  This parameter wraps-up both the testing rate _and_ the proportion of asymptomatic cases together.  Doubling this parameter still gives a reasonable fit to the data but has a huge effect on the surge of cases when lockdown is lifted.  If there are a lot of asymptomatic cases who don't get tested, then many more of the population will become immune before we lift lockdown.  But if there are very few asymptomatic cases, then a low proportion of the population becomes immune in the same time.

The hospitalisation rate of positively tested cases is calculated by fixing the maximum hospitalisation level to 25,000 based on predictions from the professional Imperial College model.

A scenario is modelled where the lockdown of April 2020 is continued until August 2020.  Assuming 7% of cases are symptomatic, tested and test positive, then it looks like by August 2020 we still haven't established herd-immunity to lift lockdown.  By August, only 30% of the population are immune.  

In this scenario, lifting the lockdown in August for 3 weeks takes the hospitalisation rate back up to 25,000 cases but gets the immunity up to 36%.   Reintroducing full lockdown again for a month gets the hospitalisation back down again.  Lifting the lockdown againt for a full month this time then gets us to 42% of the population being immune.  By repeating the lockdown, release, lockdown, release we can keep the number of hospitalised cases below 25,000 and eventually reach herd-immunity in early 2021.  

If we don't lift the lockdown, then we have to use other strategies such as testing, contact-tracing or vaccination.

## Charts for 7% symptomatic and positive-test scenario
![Hospitalisation](Hospitalised.png?raw=true "Hospitalisation")
![Immune](Immune.png?raw=true "Immune")
![Positive Test Rate](PositiveTestRate.png?raw=true "Positive Test Rate")
![Fatality Rate](FatalityRate.png?raw=true "Fatality Rate")
![Deceased](Deceased.png?raw=true "Deceased")
![Infected](Infected.png?raw=true "Infected")


