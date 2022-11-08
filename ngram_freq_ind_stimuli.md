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
install_github("seancarmody/ngramr")
library(ngramr)
library(ggplot2)
library(tidyverse)
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
Janitor <-ngram("Janitor", corpus = "en-2019", year_start = 2000, year_end = 2019,smoothing = 3, case_ins = FALSE)
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
officeClerk<- ngram(c("Office+Clerk"), year_start = 2000, corpus ="en-2019", year_end = 2019, smoothing = 3, case_ins = FALSE) 
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
as.data.frame(freq)
```

    ##                          freq
    ## accProf                    NA
    ## adminassi           -9.817839
    ## aircaptain                 NA
    ## architect                  NA
    ## armygeneral                NA
    ## babysitter                 NA
    ## Basketball         -13.516440
    ## burgerKing         -10.618268
    ## busDriver                  NA
    ## Business            -9.816041
    ## cafeteria          -10.522107
    ## cardiologist       -14.625474
    ## carpenter                  NA
    ## CEO                        NA
    ## chemEng                    NA
    ## childPsychologist          NA
    ## civilEng                   NA
    ## collegedrop                NA
    ## congressm                  NA
    ## constructionWorker         NA
    ## counselor          -12.180363
    ## creative           -12.092360
    ## criminal                   NA
    ## cs                  -9.403808
    ## dataanalyst                NA
    ## electrician                NA
    ## elemteacher                NA
    ## Engineer           -12.414395
    ## englishProf         -8.518333
    ## executive                  NA
    ## factoryWorker              NA
    ## fashion                    NA
    ## firefighter                NA
    ## flightAttendant            NA
    ## florist                    NA
    ## forkliftDriver             NA
    ## hairdresser                NA
    ## highdrop           -13.577706
    ## hiphop             -12.536458
    ## housecleaner               NA
    ## housekeeper                NA
    ## industrialEng      -16.640846
    ## Janitor                    NA
    ## jazzMus                    NA
    ## landscaper                 NA
    ## lawClerk                   NA
    ## lawyer                     NA
    ## librarian                  NA
    ## mainWorker         -10.121093
    ## mathProf           -10.607085
    ## Mcdo                       NA
    ## midwife                    NA
    ## mua                -11.797668
    ## nailtech                   NA
    ## neurologist                NA
    ## neurosurgeon               NA
    ## nurse                      NA
    ## officeClerk                NA
    ## phlProf                    NA
    ## poet                       NA
    ## president                  NA
    ## preTeacher                 NA
    ## psychologist       -12.192800
    ## psyProf             -9.805441
    ## pt                  -8.922185
    ## rapper             -14.832015
    ## realestate          -8.181804
    ## schoolCounselor            NA
    ## secretary                  NA
    ## socialwork                 NA
    ## speechpath          -9.720741
    ## teachingAssistant          NA
    ## techConsul                 NA
    ## therapist                  NA
    ## traincond                  NA
    ## unemployed         -11.987869
    ## wallTiler                  NA
    ## weightlifter               NA
    ## Yoga               -12.970686

``` r
summary(freq)
```

    ##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max.    NA's 
    ## -16.641 -12.536 -11.798 -11.497  -9.816  -8.182      54

``` r
t.test(freq)
```

    ## 
    ##  One Sample t-test
    ## 
    ## data:  freq
    ## t = -27.042, df = 24, p-value < 2.2e-16
    ## alternative hypothesis: true mean is not equal to 0
    ## 95 percent confidence interval:
    ##  -12.37426 -10.61933
    ## sample estimates:
    ## mean of x 
    ## -11.49679

p value of the t-test is not less than 0.05 so this suggests that there
is no significant difference in the word frequency in my stimuli
