# Plot Dummy Data

This repo was made specifically for use with typicode's [My JSON Server], a
simple restful API mapped to this repo's `db.json` file. Of note is that [My JSON Server] has a limit of a `10KB` `db.json` file. Hence this data is not _interesting_ to plot. Rather, like typicode proper, provides structure of data
that may be used for testing / prototyping with an actual api.

It can be accessed at:

https://my-json-server.typicode.com/sumneuron/plot-dummy-data/


## db.json

As of now db.json consists of several collections (outer keys), each of which
correspond to an SQL-esque like JSON value.

### Collections
At the moment `db.json` has the following collections:

1. Cities
2. Weather
3. Profiles

#### Cities
Cities consists of 36 records with the following structure:
```
"<id>": {
  "population": <int>,
  "country"   : <str>,
  "city"      : <str>
},
```
The cities collection is suitable for a simple or grouped bar chart.
There are five different countries. Each of which has a different number of
cities.


#### Weather
Weather consists of 19 records with the following structure:
```
"<id>": {
  "day"        : <int>,
  "month"      : <int>,
  "year"       : <int>,
  "temperature": <float>,
  "city"       : <str>
},
```
There are two different cities. This is suitable for time-series / line plot.


#### Profiles
Profiles consists of 4 records with the following structure:
```
"<id>": {
  "name"     : <str>,
  "weight"   : <float>,
  "height"   : <float>,
  "sex"      : <str>,
  "birthdate": {
    "day"  : <int>,
    "month": <int>,
    "year" : <int>
  }
},
```
Profiles can be used for bubble charts (e.g. weight v height),
bar charts (e.g. by gender), histograms (e.g. weight by birthdate)


[My JSON Server]: https://my-json-server.typicode.com/
