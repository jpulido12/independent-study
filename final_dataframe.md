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

    ## Warning: package 'usethis' was built under R version 4.1.2

``` r
install_github("seancarmody/ngramr")
```

    ## Skipping install of 'ngramr' from a github remote, the SHA1 (7facdc6f) has not changed since last install.
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

#r:sent The following code blocks will get the avg frequencies of each
stimuli in race:sentences. First, I will limit the year’s range to 2000
to 2019. Then, I qill get the average frequencty from 2000 to 2019 for
each word or phrase and store it in a variable/object.Then, I will
calculate the natural log of the average frequencies of each word. Then,
I will create a table/tibble of all the variables containing the natural
log of average frequencies for each word. After, I will plot this table
in a graph.

#janitor:rsent

``` r
Janitor <- ngram("Janitor", corpus = "en-2019", year_start = 2000, year_end = 2019,smoothing = 3, case_ins = FALSE)
Janitor <- mean(Janitor$Frequency) #calculate mean
Janitor <-log(Janitor) #calculate log
```

#engineer:rsent

``` r
Engineer <- ngram(c("Engineer"), corpus = "en-2019", year_start = 2000, year_end = 2019, smoothing = 3, case_ins = FALSE)
Engineer <- mean(Engineer$Frequency) #calculate mean
Engineer<- log(Engineer) #calculate log
```

#basketball:rsent

``` r
Basketball <- ngram(c("Basketball"), corpus = "en-2019", year_start = 2000, year_end = 2019, smoothing = 3, case_ins = FALSE)
Basketball <- mean(Basketball$Frequency) #calculate mean
Basketball <- log(Basketball) #calculate log
```

#yoga:rsent

``` r
Yoga<- ngram(c("Yoga"), corpus = "en-2019", year_start = 2000, year_end = 2019, smoothing = 3, case_ins = FALSE)
Yoga <- mean(Yoga$Frequency) #calculate mean 
Yoga <- log(Yoga) #calculate log
```

#business:rsent

``` r
Business<- ngram(c("Business"), corpus = "en-2019", year_start = 2000, year_end = 2019, smoothing = 3, case_ins = FALSE)
Business <- mean(Business$Frequency) #calculate mean
Business <- log(Business) #calculate log
```

#mcdonalds:rsent

``` r
Mcdo<- ngram(c("McDonalds+worker"), corpus = "en-2019", year_start = 2000, year_end = 2019, smoothing = 3, case_ins = FALSE)
Mcdo<- mean(Mcdo$Frequency) #calculate mean 
Mcdo <- log(Mcdo) #calculate log
```

#creative:rsent

``` r
Creative<- ngram(c("Creative"), corpus = "en-2019", year_start = 2000, year_end = 2019, smoothing = 3, case_ins = FALSE)
Creative<- mean(Creative$Frequency) #calculate mean
Creative <- log(Creative) #calculate log
```

#nailtech:rsent

``` r
nailtech <- ngram(c("Nail+tech"), corpus = "en-2019",year_start = 2000,year_end = 2019, smoothing = 3, case_ins = FALSE)
nailtech <- mean(nailtech$Frequency) #calculate mean 
nailtech<- log(nailtech) #calculate log
```

#cardiologist:rsent

``` r
cardiologist<- ngram(c("cardiologist"), corpus = "en-2019",year_start = 2000, year_end = 2019, smoothing = 3, case_ins = FALSE)
cardiologist<- mean(cardiologist$Frequency) #calculate mean 
cardiologist<- log(cardiologist) #calculate log
```

#rapper:rsent

``` r
rapper<- ngram(c("rapper"),corpus = "en-2019",year_start = 2000, year_end = 2019, smoothing = 3, case_ins = FALSE)
rapper<- mean(rapper$Frequency) #calculate mean 
rapper<- log(rapper) #calculate log
```

#cafeteria:rsent

``` r
cafeteria<- ngram(c("cafeteria+worker"),corpus = "en-2019", year_start = 2000, year_end = 2019, smoothing = 3, case_ins = FALSE)
cafeteria<- mean(cafeteria$Frequency) #calculate mean 
cafeteria<- log(cafeteria) #calculate log
```

#psycholgist:rsent

``` r
psychologist<- ngram(c("psychologist"), year_start = 2000, year_end = 2019, smoothing = 3, case_ins = FALSE)
psychologist<- mean(psychologist$Frequency) #calculate mean 
psychologist<- log(psychologist) #calculate log
```

#hiphop:rsent

``` r
hiphop<- ngram(c("hiphop+dancer"), year_start = 2000, year_end = 2019, smoothing = 3, case_ins = FALSE)
hiphop<- mean(hiphop$Frequency) #calculate mean 
hiphop<- log(hiphop) #calculate log
```

#cs:rsent

``` r
cs<- ngram(c("computer+scientist"), year_start = 2000, year_end = 2019, smoothing = 3, case_ins = FALSE)
cs<- mean(cs$Frequency) #calculate mean 
cs<- log(cs) #calculate log
```

#counselor:rsent

``` r
counselor<- ngram(c("counselor"), year_start = 2000, year_end = 2019, smoothing = 3, case_ins = FALSE)
counselor<- mean(counselor$Frequency) #calculate mean 
counselor<- log(counselor) #calculate log
```

#physical therapist:rsent

``` r
pt<- ngram(c("physical+therapist"), year_start = 2000, year_end = 2019, smoothing = 3, case_ins = FALSE)
pt<- mean(pt$Frequency) #calculate mean 
pt<- log(pt) #calculate log
```

#unemployed:rsent

``` r
unemployed<- ngram(c("unemployed"), year_start = 2000, year_end = 2019, smoothing = 3, case_ins = FALSE)
unemployed<- mean(unemployed$Frequency) #calculate mean 
unemployed<- log(unemployed) #calculate log
```

#Burgerking:rsent

``` r
burgerKing<- ngram(c("burgerking+worker"), year_start = 2000, year_end = 2019, smoothing = 3, case_ins = FALSE)
burgerKing<- mean(burgerKing$Frequency) #calculate mean 
burgerKing<- log(burgerKing) #calculate log
```

#EnglishProfessor:rsent

``` r
englishProf<- ngram(c("English+Professor"), year_start = 2000, year_end = 2019, smoothing = 3, case_ins = FALSE)
englishProf<- mean(englishProf$Frequency) #calculate mean 
englishProf<- log(englishProf) #calculate log
```

#AdministrativeAssistant:rsent

``` r
adminassi<- ngram(c("administrative+assistant"), year_start = 2000, year_end = 2019, smoothing = 3, case_ins = FALSE)
adminassi<- mean(adminassi$Frequency) #calculate mean 
adminassi<- log(adminassi) #calculate log
```

#MathematichsProfessor:rsent

``` r
mathProf<- ngram(c("Mathematics+Professor"), year_start = 2000, year_end = 2019, smoothing = 3, case_ins = FALSE)
mathProf<- mean(mathProf$Frequency) #calculate mean 
mathProf<- log(mathProf) #calculate log
```

#speechpathologist:rsent

``` r
speechpath<- ngram(c("speech+pathologist"), year_start = 2000, year_end = 2019, smoothing = 3, case_ins = FALSE)
speechpath<- mean(speechpath$Frequency) #calculate mean 
speechpath<- log(speechpath) #calculate log
```

#realestate:rsent

``` r
realestate<- ngram(c("real+estate+agent"), year_start = 2000, year_end = 2019, smoothing = 3, case_ins = FALSE)
realestate<- mean(realestate$Frequency) #calculate mean 
realestate<- log(realestate) #calculate log
```

#highschooldropout:rsent

``` r
highdrop<- ngram(c("highschool+dropout"), year_start = 2000, year_end = 2019, smoothing = 3, case_ins = FALSE)
highdrop<- mean(highdrop$Frequency) #calculate mean 
highdrop<- log(highdrop) #calculate log
```

#PsychologyProfessor:rsent

``` r
psyProf<- ngram(c("psychology+Professor"), year_start = 2000, year_end = 2019, smoothing = 3, case_ins = FALSE)
psyProf<- mean(psyProf$Frequency) #calculate mean 
psyProf<- log(psyProf) #calculate log
```

#BusDriver:rsent

``` r
busDriver<- ngram(c("bus+driver"), year_start = 2000, year_end = 2019, smoothing = 3, case_ins = FALSE)
busDriver<- mean(busDriver$Frequency) #calculate mean 
busDriver<- log(busDriver) #calculate log
```

#Techconsultant:rsent

``` r
techConsul<- ngram(c("tech+consultant"), year_start = 2000, year_end = 2019, smoothing = 3, case_ins = FALSE)
techConsul<- mean(techConsul$Frequency) #calculate mean 
techConsul<- log(techConsul) #calculate log
```

#pilatesinstructor:rsent

``` r
pilates<- ngram(c("pilates+instructor"), year_start = 2000, year_end = 2019, smoothing = 3, case_ins = FALSE)
pilates<- mean(pilates$Frequency) #calculate mean 
pilates<- log(pilates) #calculate log
```

#poet:rsent

``` r
poet<- ngram(c("poet"), year_start = 2000, year_end = 2019, smoothing = 3, case_ins = FALSE)
poet<- mean(poet$Frequency) #calculate mean 
poet<- log(poet) #calculate log
```

#congressman:rsent

``` r
congressm<- ngram(c("congressman"), year_start = 2000, year_end = 2019, smoothing = 3, case_ins = FALSE)
congressm<- mean(congressm$Frequency) #calculate mean 
congressm<- log(congressm) #calculate log
```

#trainconductor:rsent

``` r
traincond<- ngram(c("train+conductor"), year_start = 2000, year_end = 2019, smoothing = 3, case_ins = FALSE)
traincond<- mean(traincond$Frequency) #calculate mean 
traincond<- log(traincond) #calculate log
```

#socialworker:rsent

``` r
socialwork<- ngram(c("social+worker"), year_start = 2000, year_end = 2019, smoothing = 3, case_ins = FALSE)
socialwork<- mean(socialwork$Frequency) #calculate mean 
socialwork<- log(socialwork) #calculate log
```

#collegedropout:rsent

``` r
collegedrop<- ngram(c("Dropout"), year_start = 2000, year_end = 2019, smoothing = 3, case_ins = FALSE)
collegedrop<- mean(collegedrop$Frequency) #calculate mean 
collegedrop<- log(collegedrop) #calculate log
```

#civilengineer:rsent

``` r
civileng<- ngram(c("civil+engineer"), year_start = 2000, year_end = 2019, smoothing = 3, case_ins = FALSE)
civileng<- mean(civileng$Frequency) #calculate mean 
civileng<- log(civileng) #calculate log
```

#philosophyprofessor:rsent

``` r
phlProf<- ngram(c("philosophy+professor"), year_start = 2000, year_end = 2019, smoothing = 3, case_ins = FALSE)
phlProf<- mean(phlProf$Frequency) #calculate mean 
phlProf<- log(phlProf) #calculate log
```

#maintenanceworker:rsent

``` r
mainWorker<- ngram(c("maintenance+worker"), year_start = 2000, year_end = 2019, smoothing = 3, case_ins = FALSE)
mainWorker<- mean(mainWorker$Frequency) #calculate mean 
mainWorker<- log(mainWorker) #calculate log
```

#housekeeper:rsent

``` r
housekeeper<- ngram(c("housekeeper"), year_start = 2000, year_end = 2019, smoothing = 3, case_ins = FALSE)
housekeeper<- mean(housekeeper$Frequency) #calculate mean 
housekeeper<- log(housekeeper) #calculate log
```

#secretary:rsent

``` r
secretary<- ngram(c("secretary"), year_start = 2000, year_end = 2019, smoothing = 3, case_ins = FALSE)
secretary<- mean(secretary$Frequency) #calculate mean 
secretary<- log(secretary) #calculate log
```

#criminal:rsent

``` r
criminal<- ngram(c("criminal"), year_start = 2000, year_end = 2019, smoothing = 3, case_ins = FALSE)
criminal<- mean(criminal$Frequency) #calculate mean 
criminal<- log(criminal) #calculate log
```

#lawyer:rsent

``` r
lawyer<- ngram(c("lawyer"), year_start = 2000, year_end = 2019, smoothing = 3, case_ins = FALSE)
lawyer<- mean(lawyer$Frequency) #calculate mean 
lawyer<- log(lawyer) #calculate log
```

#lawclerk:rsent

``` r
lawClerk<- ngram(c("law+clerk"), year_start = 2000, year_end = 2019, smoothing = 3, case_ins = FALSE)
lawClerk<- mean(lawClerk$Frequency) #calculate mean 
lawClerk<- log(lawClerk) #calculate log
```

#AccountingProfessor:rsent

``` r
accProf<- ngram(c("accounting+Professor"), year_start = 2000, year_end = 2019, smoothing = 3, case_ins = FALSE)
accProf<- mean(accProf$Frequency) #calculate mean 
accProf<- log(accProf) #calculate log
```

#jazzmusician:rsent

``` r
jazzMus<- ngram(c("jazz+musician"), year_start = 2000, year_end = 2019, smoothing = 3, case_ins = FALSE)
jazzMus<- mean(jazzMus$Frequency) #calculate mean 
jazzMus<- log(jazzMus) #calculate log
```

#gender:sent The following code blocks will get the avg frequencies of
each stimuli in gender:sentences. First, I will limit the year’s range
to 2000 to 2019. Then, I qill get the average frequencty from 2000 to
2019 for each word or phrase and store it in a variable/object.Then, I
will calculate the natural log of the average frequencies of each word.
Then, I will create a table/tibble of all the variables containing the
natural log of average frequencies for each word. After, I will plot
this table in a graph.

#Hairdresser:gsent

``` r
hairdresser<- ngram(c("hairdresser"), year_start = 2000, year_end = 2019, smoothing = 3, case_ins = FALSE)
hairdresser<- mean(hairdresser$Frequency) #calculate mean 
hairdresser<- log(hairdresser) #calculate log
```

#CEO:gsent

``` r
CEO<- ngram(c("CEO"), year_start = 2000, year_end = 2019, smoothing = 3, case_ins = FALSE)
CEO<- mean(CEO$Frequency) #calculate mean 
CEO<- log(CEO) #calculate log
```

#Housecleaner:gsent

``` r
housecleaner<- ngram(c("housecleaner"), year_start = 2000, year_end = 2019, smoothing = 3, case_ins = FALSE)
housecleaner<- mean(housecleaner$Frequency) #calculate mean 
housecleaner<- log(housecleaner) #calculate log
```

#Data analyst:gsent

``` r
dataanalyst<- ngram(c("data+analyst"), year_start = 2000, year_end = 2019, smoothing = 3, case_ins = FALSE)
dataanalyst<- mean(dataanalyst$Frequency) #calculate mean 
dataanalyst<- log(dataanalyst) #calculate log
```

#Elementaryteacher:gsent

``` r
elemteacher<- ngram(c("elementary+teacher"), year_start = 2000, year_end = 2019, smoothing = 3, case_ins = FALSE)
elemteacher<- mean(elemteacher$Frequency) #calculate mean 
elemteacher<- log(elemteacher) #calculate log
```

#President:gsent

``` r
president<- ngram(c("president"), year_start = 2000, year_end = 2019, smoothing = 3, case_ins = FALSE)
president<- mean(president$Frequency) #calculate mean 
president<- log(president) #calculate log
```

#nursing:gsent

``` r
nurse<- ngram(c("nurse"), year_start = 2000, year_end = 2019, smoothing = 3, case_ins = FALSE)
nurse<- mean(nurse$Frequency) #calculate mean 
nurse<- log(nurse) #calculate log
```

#Business:gsent

``` r
executive<- ngram(c("business+executive"), year_start = 2000, year_end = 2019, smoothing = 3, case_ins = FALSE)
executive<- mean(executive$Frequency) #calculate mean 
executive<- log(executive) #calculate log
```

#Fashion:gsent

``` r
fashion<- ngram(c("fashion+major"), year_start = 2000, year_end = 2019, smoothing = 3, case_ins = FALSE)
fashion<- mean(fashion$Frequency) #calculate mean 
fashion<- log(fashion) #calculate log
```

#Neurologist:gsent

``` r
neurologist<- ngram(c("Neurologist"), year_start = 2000, year_end = 2019, smoothing = 3, case_ins = FALSE)
neurologist<- mean(neurologist$Frequency) #calculate mean 
neurologist<- log(neurologist) #calculate log
```

#preschool:gsent

``` r
preTeacher<- ngram(c("preschool+teacher"), year_start = 2000, year_end = 2019, smoothing = 3, case_ins = FALSE)
preTeacher<- mean(preTeacher$Frequency) #calculate mean 
preTeacher<- log(preTeacher) #calculate log
```

#Chemical engineer:gsent

``` r
chemEng<- ngram(c("chemical+engineer"), year_start = 2000, year_end = 2019, smoothing = 3, case_ins = FALSE)
chemEng<- mean(chemEng$Frequency) #calculate mean 
chemEng<- log(chemEng) #calculate log
```

#makeupartist:gsent

``` r
mua<- ngram(c("makeup+artist"), year_start = 2000, year_end = 2019, smoothing = 3, case_ins = FALSE)
mua<- mean(mua$Frequency) #calculate mean 
mua<- log(mua) #calculate log
```

#Babysitter:gsent

``` r
babysitter<- ngram(c("babysitter"), year_start = 2000, year_end = 2019, smoothing = 3, case_ins = FALSE)
babysitter<- mean(babysitter$Frequency) #calculate mean 
babysitter<- log(babysitter) #calculate log
```

#weightlifter:gsent

``` r
weightlifter<- ngram(c("weightlifter"), year_start = 2000, corpus = "en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE)
weightlifter<- mean(weightlifter$Frequency) #calculate mean 
weightlifter<- log(weightlifter) #calculate log
```

#midwife:gsent

``` r
midwife<- ngram(c("midwife"), year_start = 2000, corpus = "en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE)
midwife<- mean(midwife$Frequency) #calculate mean 
midwife<- log(midwife) #calculate log
```

#Neurosurgeon:gsent

``` r
neurosurgeon<- ngram(c("neurosurgeon"), year_start = 2000, corpus = "en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE)
neurosurgeon<- mean(neurosurgeon$Frequency) #calculate mean 
neurosurgeon<- log(neurosurgeon) #calculate log
```

#ArmyGeneral:gsent

``` r
armygeneral<- ngram(c("army+general"), year_start = 2000, corpus = "en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE)
armygeneral<- mean(armygeneral$Frequency) #calculate mean 
armygeneral<- log(armygeneral) #calculate log
```

#Industrial:gsent

``` r
industrialEng<- ngram(c("Industrial+Engineer"), year_start = 2000, corpus = "en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE)
industrialEng<- mean(industrialEng$Frequency) #calculate mean 
industrialEng<- log(industrialEng) #calculate log
```

#Librarian:gsent

``` r
librarian<- ngram(c("librarian"), year_start = 2000, corpus = "en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE)
librarian<- mean(librarian$Frequency) #calculate mean 
librarian<- log(librarian) #calculate log
```

#Captain:gsent

``` r
aircaptain<- ngram(c("Airforce+Captain"), year_start = 2000, corpus = "en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE)
aircaptain<- mean(aircaptain$Frequency) #calculate mean 
aircaptain<- log(aircaptain) #calculate log
```

#Carpenter:gsent

``` r
carpenter<- ngram(c("Carpenter"), year_start = 2000, corpus = "en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE)
carpenter<- mean(carpenter$Frequency) #calculate mean 
carpenter<- log(carpenter) #calculate log
```

#Teaching:gsent

``` r
teachingAssistant<- ngram(c("Teaching+Assistant"), year_start = 2000, corpus ="en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE) 
teachingAssistant<- mean(teachingAssistant$Frequency) #calculate mean 
teachingAssistant<- log(teachingAssistant) #calculate log
```

#Therapist:gsent

``` r
therapist<- ngram(c("Therapist"), year_start = 2000, corpus ="en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE) 
therapist<- mean(therapist$Frequency) #calculate mean 
therapist<- log(therapist) #calculate log
```

#Firefighter:gsent

``` r
firefighter<- ngram(c("Firefighter"), year_start = 2000, corpus ="en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE) 
firefighter<- mean(firefighter$Frequency) #calculate mean 
firefighter<- log(firefighter) #calculate log
```

#Child:gsent

``` r
childPsychologist<- ngram(c("Child+Psychologist"), year_start = 2000, corpus ="en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE) 
childPsychologist<- mean(childPsychologist$Frequency) #calculate mean 
childPsychologist<- log(childPsychologist) #calculate log
```

#Architect:gsent

``` r
architect<- ngram(c("architect"), year_start = 2000, corpus ="en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE) 
architect<- mean(architect$Frequency) #calculate mean 
architect<- log(architect) #calculate log
```

#Flight:gsent

``` r
flightAttendant<- ngram(c("flight+Attendant"), year_start = 2000, corpus ="en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE) 
flightAttendant<- mean(flightAttendant$Frequency) #calculate mean 
flightAttendant<- log(flightAttendant) #calculate log
```

#School:gsent

``` r
schoolCounselor<- ngram(c("School+Counselor"), year_start = 2000, corpus ="en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE) 
schoolCounselor<- mean(schoolCounselor$Frequency) #calculate mean 
schoolCounselor<- log(schoolCounselor) #calculate log
```

#Landscaper:gsent

``` r
landscaper<- ngram(c("landscaper"), year_start = 2000, corpus ="en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE) 
landscaper<- mean(landscaper$Frequency) #calculate mean 
landscaper<- log(landscaper) #calculate log
```

#Sewing:gsent

``` r
factoryWorker<- ngram(c("Factory+Worker"), year_start = 2000, corpus ="en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE) 
factoryWorker<- mean(factoryWorker$Frequency) #calculate mean 
factoryWorker<- log(factoryWorker) #calculate log
```

#Electrician:gsent

``` r
electrician<- ngram(c("Electrician"), year_start = 2000, corpus ="en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE) 
electrician<- mean(electrician$Frequency) #calculate mean 
electrician<- log(electrician) #calculate log
```

#Florist:gsent

``` r
florist <- ngram(c("florist"), year_start = 2000, corpus ="en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE) 
florist<- mean(florist$Frequency) #calculate mean 
florist<- log(florist) #calculate log
```

#Construction:gsent

``` r
constructionWorker<- ngram(c("Construction+Worker"), year_start = 2000, corpus ="en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE) 
constructionWorker<- mean(constructionWorker$Frequency) #calculate mean 
constructionWorker<- log(constructionWorker) #calculate log
```

#Office:gsent

``` r
officeClerk<- ngram(c("Office+clerk"), year_start = 2000, corpus ="en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE) 
officeClerk<- mean(officeClerk$Frequency) #calculate mean 
officeClerk<- log(officeClerk) #calculate log
```

#Wall:gsent

``` r
wallTiler<- ngram(c("Wall+Tiler"), year_start = 2000, corpus ="en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE) 
wallTiler<- mean(wallTiler$Frequency) #calculate mean 
wallTiler<- log(wallTiler) #calculate log
```

#Forklift:gsent

``` r
forkliftDriver<- ngram(c("Forklift+Driver"), year_start = 2000, corpus ="en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE) 
forkliftDriver<- mean(forkliftDriver$Frequency) #calculate mean 
forkliftDriver<- log(forkliftDriver) #calculate log
```

##Part 2———

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
freq2 <- c(achievement, aggressive, ambitious, angry, authority, basketball, beggar, boss, captain, ceo, cocaine, colonizer, congressman, cop, criminal, dancer, diabetes, doctor, engineer, entitlement, gang, general, healthcare, hiphop, homeless, ignorant, industrious, janitor, lazy, loud, musical, nurturing, poverty, privilege, professor, progressive, purity, racist, rap, redneck, researcher, rnb, scientist, spices, struggling, teenmom, thief, unseasoned, villain, violence)

names(freq2)[1] <- "achievement"
names(freq2)[2] <- "aggressive"
names(freq2)[3] <- "ambitious"
names(freq2)[4] <- "angry"
names(freq2)[5] <- "authority"
names(freq2)[6] <- "basketball"
names(freq2)[7] <- "beggar"
names(freq2)[8] <- "boss"
names(freq2)[9] <- "captain"
names(freq2)[10] <- "ceo"
names(freq2)[11] <- "cocaine"
names(freq2)[12] <- "colonizer"
names(freq2)[13] <- "congressman"
names(freq2)[14] <- "cop"
names(freq2)[15] <- "criminal"
names(freq2)[16] <- "dancer"
names(freq2)[17] <- "diabetes"
names(freq2)[18] <- "doctor"
names(freq2)[19] <- "engineer"
names(freq2)[20] <- "entitlement"
names(freq2)[21] <- "gang"
names(freq2)[22] <- "general"
names(freq2)[23] <- "healthcare"
names(freq2)[24] <- "hiphop"
names(freq2)[25] <- "homeless"
names(freq2)[26] <- "ignorant"
names(freq2)[27] <- "industrious"
names(freq2)[28] <- "janitor"
names(freq2)[29] <- "lazy"
names(freq2)[30] <- "loud"
names(freq2)[31] <- "musical"
names(freq2)[32] <- "nurturing"
names(freq2)[33] <- "poverty"
names(freq2)[34] <- "privilege"
names(freq2)[35] <- "professor"
names(freq2)[36] <- "progressive"
names(freq2)[37] <- "purity"
names(freq2)[38] <- "racist"
names(freq2)[39] <- "rap"
names(freq2)[40] <- "redneck"
names(freq2)[41] <- "researcher"
names(freq2)[42] <- "rnb"
names(freq2)[43] <- "scientist"
names(freq2)[44] <- "spices"
names(freq2)[45] <- "struggling"
names(freq2)[46] <- "teenmom"
names(freq2)[47] <- "thief "
names(freq2)[48] <- "unseasoned"
names(freq2)[49] <- "villain"
names(freq2)[50] <- "violence"
```

``` r
freqdataframe02<- as.data.frame(freq2)
colnames(freqdataframe02)
```

    ## [1] "freq2"

``` r
names(freqdataframe02)[names(freqdataframe02) == "freq2"] <- "freq"
```

``` r
#create vector with the objects created 
freq <- c(accProf, adminassi, aircaptain, architect, armygeneral,babysitter, Basketball, burgerKing, busDriver, Business, cafeteria,cardiologist,carpenter,CEO,chemEng,childPsychologist, civileng, collegedrop, congressm, constructionWorker, counselor, Creative, criminal, cs, dataanalyst, electrician, elemteacher, Engineer, englishProf, executive, factoryWorker, fashion, firefighter, flightAttendant, florist, forkliftDriver, hairdresser, highdrop, hiphop, housecleaner, industrialEng, Janitor, jazzMus, landscaper, lawClerk, lawyer, librarian, mainWorker, mathProf, Mcdo, midwife, mua, nailtech, neurologist, neurosurgeon, nurse, officeClerk, phlProf, pilates, poet, president, preTeacher, psychologist, psyProf, pt, rapper, realestate, schoolCounselor, secretary, socialwork, speechpath, teachingAssistant, techConsul, therapist, traincond, unemployed, wallTiler, weightlifter, Yoga)
#change names to the word 
names(freq)[1] <- "accProf"
names(freq)[2] <- "adminassi"
names(freq)[3] <- "aircaptain"
names(freq)[4] <- "architect"
names(freq)[5] <- "armygeneral"
names(freq)[6] <- "babysitter"
names(freq)[7] <- "Basketball"
names(freq)[8] <- "burgerKing"
names(freq)[9] <- "busDriver"
names(freq)[10] <- "Business"
names(freq)[11] <- "cafeteria"
names(freq)[12] <- "cardiologist"
names(freq)[13] <- "carpenter"
names(freq)[14] <- "CEO"
names(freq)[15] <- "chemEng"
names(freq)[16] <- "childPsychologist"
names(freq)[17] <- "civilEng"
names(freq)[18] <- "collegedrop"
names(freq)[19] <- "congressm"
names(freq)[20] <- "constructionWorker"
names(freq)[21] <- "counselor"
names(freq)[22] <- "creative"
names(freq)[23] <- "criminal"
names(freq)[24] <- "cs"
names(freq)[25] <- "dataanalyst"
names(freq)[26] <- "electrician"
names(freq)[27] <- "elemteacher"
names(freq)[28] <- "Engineer"
names(freq)[29] <- "englishProf"
names(freq)[30] <- "executive"
names(freq)[31] <- "factoryWorker"
names(freq)[32] <- "fashion"
names(freq)[33] <- "firefighter"
names(freq)[34] <- "flightAttendant"
names(freq)[35] <- "florist"
names(freq)[36] <- "forkliftDriver"
names(freq)[37] <- "hairdresser"
names(freq)[38] <- "highdrop"
names(freq)[39] <- "hiphop"
names(freq)[40] <- "housecleaner"
names(freq)[41] <- "housekeeper"
names(freq)[42] <- "industrialEng"
names(freq)[43] <- "Janitor"
names(freq)[44] <- "jazzMus"
names(freq)[45] <- "landscaper"
names(freq)[46] <- "lawClerk"
names(freq)[47] <- "lawyer"
names(freq)[48] <- "librarian"
names(freq)[49] <- "mainWorker"
names(freq)[50] <- "mathProf"
names(freq)[51] <- "Mcdo"
names(freq)[52] <- "midwife"
names(freq)[53] <- "mua"
names(freq)[54] <- "nailtech"
names(freq)[55] <- "neurologist"
names(freq)[56] <- "neurosurgeon"
names(freq)[57] <- "nurse"
names(freq)[58] <- "officeClerk"
names(freq)[59] <- "phlProf"
names(freq)[60] <- "poet"
names(freq)[61] <- "president"
names(freq)[62] <- "preTeacher"
names(freq)[63] <- "psychologist"
names(freq)[64] <- "psyProf"
names(freq)[65] <- "pt"
names(freq)[66] <- "rapper"
names(freq)[67] <- "realestate"
names(freq)[68] <- "schoolCounselor"
names(freq)[69] <- "secretary"
names(freq)[70] <- "socialwork"
names(freq)[71] <- "speechpath"
names(freq)[72] <- "teachingAssistant"
names(freq)[73] <- "techConsul"
names(freq)[74] <- "therapist"
names(freq)[75] <- "traincond"
names(freq)[76] <- "unemployed"
names(freq)[77] <- "wallTiler"
names(freq)[78] <- "weightlifter"
names(freq)[79] <- "Yoga"
View(freq)
```

``` r
freqdataframe<-as.data.frame(freq)
#summary(freq)
```

``` r
finalDataFrame<-rbind(freqdataframe, freqdataframe02)
summary(finalDataFrame)
```

    ##       freq        
    ##  Min.   :-18.587  
    ##  1st Qu.:-13.903  
    ##  Median :-11.852  
    ##  Mean   :-12.182  
    ##  3rd Qu.:-10.428  
    ##  Max.   : -7.967

``` r
mean<- -12.182
```

``` r
t.test(finalDataFrame$freq, mu = mean )
```

    ## 
    ##  One Sample t-test
    ## 
    ## data:  finalDataFrame$freq
    ## t = -0.00080098, df = 128, p-value = 0.9994
    ## alternative hypothesis: true mean is not equal to -12.182
    ## 95 percent confidence interval:
    ##  -12.60181 -11.76253
    ## sample estimates:
    ## mean of x 
    ## -12.18217

p value of the t-test is not less than 0.05 so this suggests that there
is no significant difference in the word frequency in my stimuli
