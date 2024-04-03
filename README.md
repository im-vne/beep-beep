# beep-beep
taxis and stuff


## Explanation of Files

- Above, we have a folder containing the Cleaned Data for each day of interest (in the folder named Cleaned), as well as the Cleaned Data merged with the Demographic Data- in addition to some other information (in the folder named Final).
- The fullTrainData and fullTestData are constructed such that each of the 6 time chunks in each of our 12 days has 75 randomly chosen observations in the Train Data, and 25 randomly chosen observations in the Test Data. These are the files that are meant to be used in model construction and analysis.
- Additionally, the data dictionary serves to explain some of the terms seen in the _Final file, as some of the variables are encoded on an unitutitive, numeric scale that makes no sense when you look at it.

## Data Cleaning

In order to clean this data, the following steps were taken:
- All taxi rides that didn't exclusively start and end on our 12 days of interest were removed.
- All taxi rides that had negative values for any variable were removed.
- All taxi rides that had a pickup or dropoff in a Taxi Zone that we didn't have demographic information (ie, that didn't have a corresponding Neighborhood Tabulation Area) were removed.
- Only Taxi Rides with a "standard rate code" were kept in (as such, the RateCodeID variable was removed).
- Only Taxi Rides that ended with Credit Card payment were kept.
- Only Taxi Rides that were not "store and foreward" were kept (such that the Store_and_fwd_flag variable was removed).
