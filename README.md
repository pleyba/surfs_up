# Surfs Up

### Overview of the analysis

This is an analysis to expose temperature trends for the months of June and December in Oahu. For a surf and ice cream shop.



### Results

There are three key differences in the weather between June and December that are shown in the two summary tables below.

* The mean temperature in June is more favorable.
* The minimum temperature in Jun is also more favorable.
* The weather in June is slightly more consistent which seems to be more favorable as well.
* 

Summary Statistics for June

![June_Temps](resources/June_Temps.PNG)



Summary Statistics for December

![December_Temps](resources//December_Temps.PNG)

### Summary

The statistics in the data indicate that business would be better and more consistent in June but not significantly better.

To improve the accuracy of the results some additional views of the data are recommended.  At a minimum the summary statistics for precipitation should be added to the analysis as shown in the two queries below.

```sql
jun_prcp_results = session.query(Measurement.date, Measurement.prcp).filter(extract('month', Measurement.date) == 6)
```

```sql
 dec_prcp_results = session.query(Measurement.date, Measurement.prcp).filter(extract('month', Measurement.date) == 12)
```

These two queries would isolate the precipitation data.  In addition to this charts and time data could be utilized provide a better view of the data and expose additional trends.