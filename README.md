
# Package title

<font size = "20">ss3sim</font>

# Location

The package can be downloaded from Cran or from Github.  

1. Cran


```r 
install.packages('ss3sim',
repos='https://cran.r-project.org/web/packages/ss3sim/index.html', dependencies=TRUE)
```

2.  Github

```r
remotes::install_github("ss3sim/ss3sim", ref = "main",
build_vignettes = TRUE, dependencies = TRUE )
```

# Vignette(s)

`{ss3sim}` has a number of useful help files.

There are three documents which are useful when working with `{ss3sim}`.
The first is the .README, which is comprehensive and offers notes on the
installation, file structure and an example simulation of the package.
The README.md can be found
[here](https://github.com/ss3sim/ss3sim/blob/main/README.md)

There are three vignettes available on the github which cover  
1)
[Introduction](https://ss3sim.github.io/ss3sim/articles/introduction.html)  
2) [Making
models](https://github.com/ss3sim/ss3sim/blob/main/vignettes/making-models.Rmd)  
3) [Modifying
models](https://github.com/ss3sim/ss3sim/blob/main/vignettes/modifying-models.Rmd).

The package is actively under development by NOAA, and as such the
[discussion board](https://github.com/ss3sim/ss3sim/discussions),on
github is particularly useful for resolving queries.

There is also an introduction [avilable on
CRAN](https://cran.r-project.org/web/packages/ss3sim/vignettes/introduction.html)
however it is deprecated and following the instructions will not allow
the user to create simulations. This is particularly problematic as when
Google is used to [search for introductory
material](https://www.google.com/search?q=introduction+to+ss3sim&oq=introduction+to+ss3sim&aqs=chrome..69i57j69i60l2.4403j0j7&sourceid=chrome&ie=UTF-8),
the CRAN intro is the first result.

# Application(s)

The primary application of the package is that it allows users to crate
simulated fish populations and estimate them using the [Stock Synthesis
3](https://nmfs-stock-synthesis.github.io/doc/SS330_User_Manual.html)
modelling framework.The package has been employed for simulation testing
documented in peer-review literature. Notable publications include:

Monnahan et al. ([2016](#ref-monnahan_effect_2016))  
Ono et al. ([2015](#ref-ono_importance_2015))  
Rudd et al. ([2021](#ref-rudd_catch_2021))

# Review

`{ss3sim}` is an r package which allows users to simulate fish stock
populations and asses them using [Stock Synthesis
3](https://nmfs-stock-synthesis.github.io/doc/SS330_User_Manual.html)
modelling framework. The package was initially developed as part of a
graduate class project in the school of Aquatic and fisheries Science ,
University of Washington, with the project being led by Sean Anderson
(Anderson et al. ([2014](#ref-anderson_ss3sim_2014))). Each simulation
has three components an Operating model (OM) which represent the true
population such as natural mortality *M*, recruitment *R* and fishing
mortality *F*,the Estimation method (EM) (Stock assessments, survey data
etc) which denotes how the population is to be assessed and the control
file, which allows the users how and when they would like to alter the
EM and OM.

While the file structure of the does appear cumbersome at first, running
a pre-specification (or boiler plate) is realities straightforward by
following the introduction vignette. The package allows users to alter
SS3 assessments in a relatively straightforward fashion,compared to
editing the large .text files which SS3 assessments use. The other nice
aspect of the package is there are three boiler plates, each mimicking a
different fish life-history pattern. The species are Cod *Gadus morhua*
, pacific anchovy *Engraulis mordax* and yellowtail founder
*Pleuronectes ferruginea* .

I would recommend the package to anyone interested in fisheries
simulation testing or with `{ss3sim}`. As a user who had no SS3
experience, I was able to alter the boiler plates and simulate the
effect of having *F* set far higher than is suitable. The effect of this
on a fishery over a time period ( I chose 100 years) could then be
observed.

# References

Anderson, S.C., Monnahan, C.C., Johnson, K.F., Ono, K., Valero, J.L.,
2014. ss3sim: An R Package for Fisheries Stock Assessment Simulation
with Stock Synthesis. PLoS ONE 9, e92725.
<https://doi.org/10.1371/journal.pone.0092725>

Monnahan, C.C., Ono, K., Anderson, S.C., Rudd, M.B., Hicks, A.C.,
Hurtado-Ferro, F., Johnson, K.F., Kuriyama, P.T., Licandeo, R.R.,
Stawitz, C.C., Taylor, I.G., Valero, J.L., 2016. The effect of length
bin width on growth estimation in integrated age-structured stock
assessments. Fisheries Research, Growth: Theory, estimation, and
application in fishery stock assessment models 180, 103–112.
<https://doi.org/10.1016/j.fishres.2015.11.002>

Ono, K., Licandeo, R., Muradian, M.L., Cunningham, C.J., Anderson, S.C.,
Hurtado-Ferro, F., Johnson, K.F., McGilliard, C.R., Monnahan, C.C.,
Szuwalski, C.S., Valero, J.L., Vert-Pre, K.A., Whitten, A.R., Punt,
A.E., 2015. The importance of length and age composition data in
statistical age-structured models for marine species. ICES Journal of
Marine Science 72, 31–43. <https://doi.org/10.1093/icesjms/fsu007>

Rudd, M.B., Cope, J.M., Wetzel, C.R., Hastie, J., 2021. Catch and Length
Models in the Stock Synthesis Framework: Expanded Application to
Data-Moderate Stocks. Frontiers in Marine Science 8, 663554.
<https://doi.org/10.3389/fmars.2021.663554>

