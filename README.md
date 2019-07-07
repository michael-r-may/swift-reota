# Swifty Rota

Swifty Rota is a simple server app (and commandline version too) that attempts solves the problem - _"who's turn is it this week to do X?"_

It does this by offering a simple `HTTP GET` API that takes a list of names and returns whichever one should be on rota for this current fortnight, by simply dividing up time into two week chunks and mapping the rota onto it. Obviously it doesn't do the "dividing up time into two week chunks" as an actual calculation across all of time but simply works it out based on the current week number in the current year (gregorian calcular only right now).

A basic all would look like 

`curl --get https://somedomain.com?names="John,Paul,Ringo,George"`

and return simply 

```
HTTP 200 OK
Ringo
```
