##Independent Study Intro The current study is Joemari Pulido’s
independent study advised by Dr. Joanna Morris. The current study aims
to explore stereotype violations using the N400 erp component. The
current script shows the code used to generate ngram frequencies of
stimuli to be used in the current study.

Sean Carmody et al. created and maintain a package ‘ngramr’ which
queries the Google Books Ngram Viewer. The Google Books Ngram Viewer
corpus holds about 2 trillion words/phrases. The specific corpus the
current study will be using is corpus ‘en-2019’ which contains data
about word frequencies from 1950 up until 2019.

The following code block loads the package ‘devtools’. Then, calls the
function ‘install_github’ which enables one to install a repository
directly from GitHub into RStudio. syntax is
‘install_github(“respositoryownner/repositoryname”)’. Then, once the
repository is loaded, load the ‘ngramr’ package into RStudio, which then
allows you to enter a list of phrases to display a graph showing how
often the phrases occurred in a given corpus.

#load necessary packages and install ngram package from seancarmody
github repository

``` r
library(devtools)
```

    ## Loading required package: usethis

``` r
install_github("seancarmody/ngramr")
```

    ## Skipping install of 'ngramr' from a github remote, the SHA1 (9856fa48) has not changed since last install.
    ##   Use `force = TRUE` to force installation

``` r
library(ngramr)
library(ggplot2)
```

    ## Warning: package 'ggplot2' was built under R version 4.1.2

``` r
library(tidyverse)
```

    ## ── Attaching packages ─────────────────────────────────────── tidyverse 1.3.1 ──

    ## ✔ tibble  3.1.8      ✔ dplyr   1.0.10
    ## ✔ tidyr   1.2.1      ✔ stringr 1.4.1 
    ## ✔ readr   2.1.2      ✔ forcats 0.5.1 
    ## ✔ purrr   0.3.5

    ## Warning: package 'tibble' was built under R version 4.1.2

    ## Warning: package 'tidyr' was built under R version 4.1.2

    ## Warning: package 'readr' was built under R version 4.1.2

    ## Warning: package 'dplyr' was built under R version 4.1.2

    ## Warning: package 'stringr' was built under R version 4.1.2

    ## ── Conflicts ────────────────────────────────────────── tidyverse_conflicts() ──
    ## ✖ dplyr::filter() masks stats::filter()
    ## ✖ dplyr::lag()    masks stats::lag()

``` r
library(SciViews)
```

syntax {r find average freq for and store in object} \<- ngram(c(““),
year_start = 2000, corpus =”en-2019”, year_end = 2019, smoothing = 3,
case_ins = FALSE) \<- mean($Frequency) #calculate mean \<- log()
#calculate log

#r:word pairs The following code blocks will get the avg frequencies of
each stimuli in race:wordpairs. First, I will limit the year’s range to
2000 to 2019. Then, I will get the average frequencty from 2000 to 2019
for each word or phrase and store it in a variable/object.Then, I will
calculate the natural log of the average frequencies of each word. Then,
I will create a table/tibble of all the variables containing the natural
log of average frequencies for each word. After, I will plot this table
in a graph.

#Engineer

``` r
engineer<- ngram(c("Engineer"), year_start = 2000, corpus ="en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE) 
engineer<- mean(engineer$Frequency) #calculate mean 
engineer<- log(engineer) #calculate log
```

#Basketball

``` r
basketball<- ngram(c("basketball"), year_start = 2000, corpus ="en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE) 
basketball<- mean(basketball$Frequency) #calculate mean 
basketball<- log(basketball) #calculate log
```

#CEO

``` r
ceo<- ngram(c("CEO"), year_start = 2000, corpus ="en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE) 
ceo<- mean(ceo$Frequency) #calculate mean 
ceo<- log(ceo) #calculate log
```

#Criminal

``` r
criminal <- ngram(c("Criminal"), year_start = 2000, corpus ="en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE) 
criminal<- mean(criminal$Frequency) #calculate mean 
criminal<- log(criminal) #calculate log
```

#Achievement

``` r
achievement<- ngram(c("Achievement"), year_start = 2000, corpus ="en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE) 
achievement<- mean(achievement$Frequency) #calculate mean 
achievement<- log(achievement) #calculate log
```

#Homeless

``` r
homeless<- ngram(c("Homeless"), year_start = 2000, corpus ="en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE) 
homeless<- mean(homeless$Frequency) #calculate mean 
homeless<- log(homeless) #calculate log
```

#Doctor

``` r
doctor<- ngram(c("Doctor"), year_start = 2000, corpus ="en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE) 
doctor<- mean(doctor$Frequency) #calculate mean 
doctor<- log(doctor) #calculate log
```

#Janitor

``` r
janitor<- ngram(c("Janitor"), year_start = 2000, corpus ="en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE) 
janitor<- mean(janitor$Frequency) #calculate mean 
janitor<- log(janitor) #calculate log
```

#Cop

``` r
cop<- ngram(c("Cop"), year_start = 2000, corpus ="en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE) 
cop<- mean(cop$Frequency) #calculate mean 
cop<- log(cop) #calculate log
```

#Thief

``` r
thief<- ngram(c("Thief"), year_start = 2000, corpus ="en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE) 
thief<- mean(thief$Frequency) #calculate mean 
thief<- log(thief) #calculate log
```

#Racist

``` r
racist<- ngram(c("Racist"), year_start = 2000, corpus ="en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE) 
racist<- mean(racist$Frequency) #calculate mean 
racist<- log(racist) #calculate log
```

#Aggresive

``` r
aggressive<- ngram(c("Aggressive"), year_start = 2000, corpus ="en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE) 
aggressive<- mean(aggressive$Frequency) #calculate mean 
aggressive<- log(aggressive) #calculate log
```

#Boss

``` r
boss<- ngram(c("Boss"), year_start = 2000, corpus ="en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE) 
boss<- mean(boss$Frequency) #calculate mean 
boss<- log(boss) #calculate log
```

#Poverty

``` r
poverty<- ngram(c("Poverty"), year_start = 2000, corpus ="en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE) 
poverty<- mean(poverty$Frequency) #calculate mean 
poverty<- log(poverty) #calculate log
```

#Redneck

``` r
redneck<- ngram(c("Red+neck"), year_start = 2000, corpus ="en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE) 
redneck<- mean(redneck$Frequency) #calculate mean 
redneck<- log(redneck) #calculate log
```

#Diabetes

``` r
diabetes<- ngram(c("Diabetes"), year_start = 2000, corpus ="en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE) 
diabetes<- mean(diabetes$Frequency) #calculate mean 
diabetes<- log(diabetes) #calculate log
```

#Professor

``` r
professor<- ngram(c("Professor"), year_start = 2000, corpus ="en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE) 
professor<- mean(professor$Frequency) #calculate mean 
professor<- log(professor) #calculate log
```

#Cocaine

``` r
cocaine<- ngram(c("Cocaine"), year_start = 2000, corpus ="en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE) 
cocaine<- mean(cocaine$Frequency) #calculate mean 
cocaine<- log(cocaine) #calculate log
```

#Unseasoned

``` r
unseasoned<- ngram(c("Unseasoned"), year_start = 2000, corpus ="en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE) 
unseasoned<- mean(unseasoned$Frequency) #calculate mean 
unseasoned<- log(unseasoned) #calculate log
```

#Spices

``` r
spices<- ngram(c("Spices"), year_start = 2000, corpus ="en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE) 
spices<- mean(spices$Frequency) #calculate mean 
spices<- log(spices) #calculate log
```

#Congressman

``` r
congressman<- ngram(c("Congressman"), year_start = 2000, corpus ="en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE) 
congressman<- mean(congressman$Frequency) #calculate mean 
congressman<- log(congressman) #calculate log
```

#rnb

``` r
rnb<- ngram(c("RNB"), year_start = 2000, corpus ="en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE) 
rnb<- mean(rnb$Frequency) #calculate mean 
rnb<- log(rnb) #calculate log
```

#Captain

``` r
captain<- ngram(c("Captain"), year_start = 2000, corpus ="en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE) 
captain<- mean(captain$Frequency) #calculate mean 
captain<- log(captain) #calculate log
```

#Gang

``` r
gang<- ngram(c("Gang"), year_start = 2000, corpus ="en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE) 
gang<- mean(gang$Frequency) #calculate mean 
gang<- log(gang) #calculate log
```

#Scientist

``` r
scientist<- ngram(c("scientist"), year_start = 2000, corpus ="en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE) 
scientist<- mean(scientist$Frequency) #calculate mean 
scientist<- log(scientist) #calculate log
```

#Lazy

``` r
lazy<- ngram(c("Lazy"), year_start = 2000, corpus ="en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE) 
lazy<- mean(lazy$Frequency) #calculate mean 
lazy<- log(lazy) #calculate log
```

#General

``` r
general<- ngram(c("General_NOUN"), year_start = 2000, corpus ="en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE) 
general<- mean(general$Frequency) #calculate mean 
general<- log(general) #calculate log
```

#Villain

``` r
villain<- ngram(c("villain"), year_start = 2000, corpus ="en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE) 
villain<- mean(villain$Frequency) #calculate mean 
villain<- log(villain) #calculate log
```

#Industrious

``` r
industrious<- ngram(c("Industrious"), year_start = 2000, corpus ="en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE) 
industrious<- mean(industrious$Frequency) #calculate mean 
industrious<- log(industrious) #calculate log
```

#Ignorant

``` r
ignorant<- ngram(c("Ignorant"), year_start = 2000, corpus ="en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE) 
ignorant<- mean(ignorant$Frequency) #calculate mean 
ignorant<- log(ignorant) #calculate log
```

#Ambitious

``` r
ambitious<- ngram(c("Ambitious"), year_start = 2000, corpus ="en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE) 
ambitious<- mean(ambitious$Frequency) #calculate mean 
ambitious<- log(ambitious) #calculate log
```

#Musical

``` r
musical<- ngram(c("Musical"), year_start = 2000, corpus ="en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE) 
musical<- mean(musical$Frequency) #calculate mean 
musical<- log(musical) #calculate log
```

#Progressive

``` r
progressive<- ngram(c("Progressive"), year_start = 2000, corpus ="en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE) 
progressive<- mean(progressive$Frequency) #calculate mean 
progressive<- log(progressive) #calculate log
```

#Dancer

``` r
dancer<- ngram(c("Dancer"), year_start = 2000, corpus ="en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE) 
dancer<- mean(dancer$Frequency) #calculate mean 
dancer<- log(dancer) #calculate log
```

#Loud

``` r
loud<- ngram(c("Loud"), year_start = 2000, corpus ="en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE) 
loud <- mean(loud$Frequency) #calculate mean 
loud<- log(loud) #calculate log
```

#Hip Hop

``` r
hiphop<- ngram(c("Hip+hop"), year_start = 2000, corpus ="en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE) 
hiphop<- mean(hiphop$Frequency) #calculate mean 
hiphop<- log(hiphop) #calculate log
```

#Authority

``` r
authority<- ngram(c("Authority"), year_start = 2000, corpus ="en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE) 
authority<- mean(authority$Frequency) #calculate mean 
authority<- log(authority) #calculate log
```

#Rap

``` r
rap<- ngram(c("Rap"), year_start = 2000, corpus ="en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE) 
rap<- mean(rap$Frequency) #calculate mean 
rap<- log(rap) #calculate log
```

#Privilege

``` r
privilege<- ngram(c("Privilege"), year_start = 2000, corpus ="en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE) 
privilege<- mean(privilege$Frequency) #calculate mean 
privilege<- log(privilege) #calculate log
```

#Violence

``` r
violence<- ngram(c("Violence"), year_start = 2000, corpus ="en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE) 
violence<- mean(violence$Frequency) #calculate mean 
violence<- log(violence) #calculate log
```

#Entitlement

``` r
entitlement<- ngram(c("entitlement"), year_start = 2000, corpus ="en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE) 
entitlement<- mean(entitlement$Frequency) #calculate mean 
entitlement<- log(entitlement) #calculate log
```

#Healthcare

``` r
healthcare<- ngram(c("healthcare"), year_start = 2000, corpus ="en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE) 
healthcare<- mean(healthcare$Frequency) #calculate mean 
healthcare<- log(healthcare) #calculate log
```

#Researcher

``` r
researcher<- ngram(c("researcher"), year_start = 2000, corpus ="en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE) 
researcher<- mean(researcher$Frequency) #calculate mean 
researcher<- log(researcher) #calculate log
```

#Teen Mom

``` r
teenmom<- ngram(c("teen+mom"), year_start = 2000, corpus ="en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE) 
teenmom<- mean(teenmom$Frequency) #calculate mean 
teenmom<- log(teenmom) #calculate log
```

#Purity

``` r
purity<- ngram(c("purity"), year_start = 2000, corpus ="en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE) 
purity<- mean(purity$Frequency) #calculate mean 
purity<- log(purity) #calculate log
```

#Beggar

``` r
beggar<- ngram(c("Beggar"), year_start = 2000, corpus ="en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE) 
beggar<- mean(beggar$Frequency) #calculate mean 
beggar<- log(beggar) #calculate log
```

#Colonizer

``` r
colonizer<- ngram(c("Colonizer"), year_start = 2000, corpus ="en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE) 
colonizer<- mean(colonizer$Frequency) #calculate mean 
colonizer<- log(colonizer) #calculate log
```

#Struggling

``` r
struggling<- ngram(c("Struggling"), year_start = 2000, corpus ="en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE) 
struggling<- mean(struggling$Frequency) #calculate mean 
struggling<- log(struggling) #calculate log
```

#Nurturing

``` r
nurturing<- ngram(c("nurturing"), year_start = 2000, corpus ="en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE) 
nurturing<- mean(nurturing$Frequency) #calculate mean 
nurturing<- log(nurturing) #calculate log
```

#Angry

``` r
angry <- ngram(c("Angry"), year_start = 2000, corpus ="en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE) 
angry<- mean(angry$Frequency) #calculate mean 
angry<- log(angry) #calculate log
```

#dataframe Create a data frame / tibble with each word and their
frequency

``` r
freq <- c(achievement, aggressive, ambitious, angry, authority, basketball, beggar, boss, captain, ceo, cocaine, colonizer, congressman, cop, criminal, dancer, diabetes, doctor, engineer, entitlement, gang, general, healthcare, hiphop, homeless, ignorant, industrious, janitor, lazy, loud, musical, nurturing, poverty, privilege, professor, progressive, purity, racist, rap, redneck, researcher, rnb, scientist, spices, struggling, teenmom, thief, unseasoned, villain, violence)
names(freq)[1] <- "achievement"
names(freq)[2] <- "aggressive"
names(freq)[3] <- "ambitious"
names(freq)[4] <- "angry"
names(freq)[5] <- "authority"
names(freq)[6] <- "basketball"
names(freq)[7] <- "beggar"
names(freq)[8] <- "boss"
names(freq)[9] <- "captain"
names(freq)[10] <- "ceo"
names(freq)[11] <- "cocaine"
names(freq)[12] <- "colonizer"
names(freq)[13] <- "congressman"
names(freq)[14] <- "cop"
names(freq)[15] <- "criminal"
names(freq)[16] <- "dancer"
names(freq)[17] <- "diabetes"
names(freq)[18] <- "doctor"
names(freq)[19] <- "engineer"
names(freq)[20] <- "entitlement"
names(freq)[21] <- "gang"
names(freq)[22] <- "general"
names(freq)[23] <- "healthcare"
names(freq)[24] <- "hiphop"
names(freq)[25] <- "homeless"
names(freq)[26] <- "ignorant"
names(freq)[27] <- "industrious"
names(freq)[28] <- "janitor"
names(freq)[29] <- "lazy"
names(freq)[30] <- "loud"
names(freq)[31] <- "musical"
names(freq)[32] <- "nurturing"
names(freq)[33] <- "poverty"
names(freq)[34] <- "privilege"
names(freq)[35] <- "professor"
names(freq)[36] <- "progressive"
names(freq)[37] <- "purity"
names(freq)[38] <- "racist"
names(freq)[39] <- "rap"
names(freq)[40] <- "redneck"
names(freq)[41] <- "researcher"
names(freq)[42] <- "rnb"
names(freq)[43] <- "scientist"
names(freq)[44] <- "spices"
names(freq)[45] <- "struggling"
names(freq)[46] <- "teenmom"
names(freq)[47] <- "thief "
names(freq)[48] <- "unseasoned"
names(freq)[49] <- "villain"
names(freq)[50] <- "violence"
View(freq)
```

``` r
freqdataframe<- as.data.frame(freq)
summary(freq)
```

    ##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
    ## -18.587 -14.391 -12.948 -13.191 -11.689  -9.141

``` r
View(freqdataframe)
```

``` r
t.test(freq)
```

    ## 
    ##  One Sample t-test
    ## 
    ## data:  freq
    ## t = -45.177, df = 49, p-value < 2.2e-16
    ## alternative hypothesis: true mean is not equal to 0
    ## 95 percent confidence interval:
    ##  -13.77755 -12.60404
    ## sample estimates:
    ## mean of x 
    ##  -13.1908

the p value of the t-test is not less that 0.05 so this suggests that
there is no significant difference in the word frequency in my stimuli
