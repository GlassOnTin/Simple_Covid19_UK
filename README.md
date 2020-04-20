# A Simple Covid-19 compartmental model for the United Kingdom
A simple (naive, empirical, student, amateur) [compartmental epidemiological model](https://en.wikipedia.org/wiki/Compartmental_models_in_epidemiology) of the Covid-19 outbreak in the United Kingdom, using the Microsoft Excel solver to optimise the parameters.

This model partitions the United Kingdom population into three situations:
* Susceptible - those who are prone to infection with Covid-19;
* Infected - those who are currently infected and contagious;
* Recovered / deceased - those who have had the virus.

The model is fitted to data collated on the [2020 coronavirus pandemic in the United Kingdom](https://en.wikipedia.org/wiki/2020_coronavirus_pandemic_in_the_United_Kingdom) wiki page.

The model fits the following parameters:
* Reproductive rate, R(t) = 2.0 before lockdown, 1.1 after lockdown;
* Case fatality rate, CFR(t) = 2% of confirmed cases;
* Proportion of cases that are tested and test positive for COVID-19 = 7% to 2%;
* Recovery rate (gamma) - 4 days to recover;
* Hospitalisation rate - 42% of postive tested cases.

To constrain the model the peak hospitalisation rate is fixed at 25,000 based on predictions from the professional Imperial College model.

The critical piece of information missing from the model is the proportion of infections that are asymptomatic.  However, it can be seen that ~5% gives the right shape to the infection rate and deceased rate curves.  Without this information it is not possible to judge the best strategy to lift the lockdown.  

A scenario is modelled where the lockdown of April 2020 is continued until August 2020.  Assuming 5% of cases are symptomatic, tested, and test positive, then it looks like by August 2020 we still haven't established herd-immunity as only 30% of the population are immune.  Lifting the lockdown in August for 3 weeks takes the hospitalisation rate back up to 25,000 cases but gets the immunity up to 36%.   Reintroducing full lockdown again for a month gets the hospitalisation back down again.  Lifting the lockdown for a full month this time then gets us to 42% of the population being immune.  By repeating the lockdown, release, lockdown, release we can keep the number of hospitalised cases below 25,000 and eventually reach herd-immunity in early 2021.  

If we don't lift the lockdown, then we have to use other strategies such as testing, contact-tracing or vaccination.

## Charts for 5% symptomatic scenario
![Hospitalisation](Hospitalised.png?raw=true "Hospitalisation")
![Immune](Immune.png?raw=true "Immune")
![Positive Test Rate](PositiveTestRate.png?raw=true "Positive Test Rate")
![Fatality Rate](FatalityRate.png?raw=true "Fatality Rate")
![Deceased](Deceased.png?raw=true "Deceased")
![Infected](Infected.png?raw=true "Infected")


