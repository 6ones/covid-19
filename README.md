# Estimating COVID-19's Rt in Real-Time (Nigeria)

Chidindu Promise Ogbonna - May 1

I came across an analysis by [Kevin Systrom](https://twitter.com/kevin) on this exact topic, [Estimating COVID-19's Rt in Real-Time](https://github.com/k-sys/covid-19/blob/master/Realtime%20R0.ipynb). But that was done on the coronavirus pandemic in the United States.
This analysis is an attempt at estimating the COVID-19s Rt in Real-Time in **Nigeria**.

Rt is a measure of the **Effective Reproduction Number**, it's the number of people who become infected for every infectious person at time _t_, the virus' actual rate transmission rate a given moment. The detection and tracking of an emerging disease can be formalized in terms of monitoring Rt, as it evolves and approaches the critical threshold `Rt > 1`. In an article referenced by Kevin, [on gradually lifting the lockdown](https://www.nytimes.com/2020/04/06/opinion/coronavirus-end-social-distancing.html), it established this metric (Rt) as a "formal framework for how governments could monitor the state of this pandemic...", performing much better than daily/weekly count of reported cases. Calculating Rt works because it tries to make up for poor reporting of cases, [where cases reported do not show the actual severity of the virus](https://medium.com/@6ones/how-is-nigeria-faring-in-the-fight-against-covid-19-f52bfc81b8a), where there are not enough test-kits to enable proper testing of the population or where cases are only reported when symptoms show.

> Policy must not be determined based on the daily count of reported cases — the tallies you read about constantly in the news — because those are unreliable. What’s needed instead is the coronavirus’s real-time, effective reproduction number, or its actual ability to spread at a particular time.

An `Rt >= 1` means the epidemic is eating deep into the society, for every infected person, another person becomes infected. At `R_t < 1`, the epidemic will **fade out**, and at `Rt = 0`, this indicates complete absence of human to human transmission, which is what we want. No matter how badly the economy is doing, the epidemic fading out should be the number one priority of any government.

Kevin noted how understanding the Rt at a national level is not useful, but rather should be done at a local level (State) to get a granular version of Rt.
Using a modified version (a process model with Gaussian noise to estimate a time varying Rt) of the solution created by [Bettencourt & Ribeiro 2008](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0002185), which uses a Bayesian approach to estimate Rt in real-time. I won't go into detail in explaining the the methods used to evaluate Rt, but you can check Kevin's [version](https://github.com/k-sys/covid-19/blob/master/Realtime%20R0.ipynb), where he explains all this.

If you want to contact me, probably tell me what I did wrong, feel free to hit me up at [chidindu@datahorror.com](mailto:chidindu@datahorror.com)

## Analysis

You can peak the full analysis in the [notebook](https://github.com/6ones/covid-19/blob/master/Real-time%20Rt%20in%20Nigeria.ipynb) or on [nbviewer](https://nbviewer.jupyter.org/github/6ones/covid-19/blob/master/Real-time%20Rt%20in%20Nigeria.ipynb)
