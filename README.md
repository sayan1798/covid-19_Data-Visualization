# covid-19_Data-Visualization

Important datset links:
1. https://raw.githubusercontent.com/CSSEGISandData/COVID-19/master/csse_covid_19_data/csse_covid_19_time_series/time_series_covid19_confirmed_global.csv

2. https://raw.githubusercontent.com/CSSEGISandData/COVID-19/master/csse_covid_19_data/csse_covid_19_time_series/time_series_covid19_deaths_global.csv

3. https://raw.githubusercontent.com/CSSEGISandData/COVID-19/master/csse_covid_19_data/csse_covid_19_time_series/time_series_covid19_recovered_global.csv

For prediction and forecasting:

1.https://covid.ourworldindata.org/data/ecdc/full_data.csv
NOTE:These datasets are updated daily.Go check out and create your own prediction and data visualization.

Basic description of the SIER model of Epidemic:

Based on the blog aricle:
https://towardsdatascience.com/social-distancing-to-slow-the-coronavirus-768292f04296

Social distancing:
Reduce person-to-person contact in order to make spreading the disease less likely.
Spread out the spread of disease in time as much as possible to allow hospitals to 
help every sick patient to minimize deaths, increase survival rate. 
Simulate the situation using SEIR epidemiological model
S = Sucsceptible
E = Exposed
I = Infected
R = Recovered
Population moves from one stage to the other. 
dS/dt = - rho * beta * S * I
dE/dt = (rho * beta * S * I) - (alpha * I)
dI/dt = (alpha * E) - (gamma * I)
dR/dt = gamma * I
N = S + E + I + R (total population is fixed)
alpha is the inverse of the incubation period (1/t_incubation)
beta is the average contact rate in the population
gamma is the inverse of the mean infectious period (1/t_infectious)
rho is the social distancing effect. (Contact rate between people)
Rho = 1 means no social distancing. 0 means everyone is locked down, no contact at all.
R0 = beta/gamma   ----- (high R0 implies faster spreading disease)
