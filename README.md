# beep-beep
taxis and stuff


## Explanation of Files

- With the above files, the one ending with _NotCleaned is essentially the raw data- containing each and every taxi ride noted on April 19th. The file ending with _Cleaned is a scrubbed version of the aforementioned uncleaned file. The actual scrubbing that was done is laid out below. Lastly, the file ending with _Final is a file that was cleaned further, with renamed columns, and the demographic information for the pickup & dropoff taxi zones included. This is likely the file to use in data analysis and modeling. 
- Additionally, the data dictionary serves to explain some of the terms seen in the _Final file, as some of the variables are encoded on an unitutitive, numeric scale that makes no sense when you look at it.

## Data Cleaning

In order to clean this data, the following steps were taken:
- All taxi rides that didn't exclusively start and end on April 19, 2021 were removed.
- All taxi rides that had negative values for any variable were removed.
- All taxi rides that had a pickup or dropoff in a Taxi Zone that we didn't have demographic information (ie, that didn't have a corresponding Neighborhood Tabulation Area) were removed.
- Only Taxi Rides with a "standard rate code" were kept in (as such, the RateCodeID variable was removed).
- Only Taxi Rides that ended with Credit Card or Cash payment were kept.
- Only Taxi Rides that were not "store and foreward" were kept (such that the Store_and_fwd_flag variable was removed).
