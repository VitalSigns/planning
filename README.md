# VitalSigns planning

@todo intro paragraph

@todo goals

## Providers
 - MyFitnessPal
 - Jawbone Up (**)
 - Withings
 - RunKeeper (**)
 - Fitbit [x]
 - MapMyRun
 - Strava (**)

(x = known to be difficult, ** = known to be good)

## Metrics
There are different *types* of metrics. And each metric might be a different type depending on the provider.

For example, weight could be an event (my weigh-in yesterday), a "current" status (my weight right now is 200 but we have history of it), and/or a property (user first name is Matt, weight is 200.)

The best option may be to differentiate different types of metrics. Possibly "property", "current", "event"? Each metric can be optionally one or multiples.

E.g. a "workout" is an event. That's it. A "weight" could be any of them. Heartrate could be an event; average heartrate could be any of them.

- Height
- Weight
- Workout
- Average Heartrate
- Steps
- Food
- @todo: Can be up to 300 (!!) metrics. We won't aim for all of em.


## Tools
 - Need a conversion class to handle conversion and standardization of measure; will need an adapter system for each systems measures. Also see https://packagist.org/packages/triplepoint/php-units-of-measure as a resource

## Weird Caveats
 - Time zones ugh
 - Rather than paginated lists, many APIs will only return based on a date query; e.g. Fitbit you have to query every date to see when there's even date available, so you need a service to query the entire user history with Fitbit *just* to see if there was data
 - Fitbit has huge rate limits--first sync can take days
 - Some services just return a colleciton of IDs and you need to pull one by one
 - Weight is sometimes an event and sometimes just a property on the profile
 - Friend (Andreas) report that it's impossible to do any analytics on a narrower-than-day level
 - Many weird versions of oAuth/etc.


## Alpha version of the plan:
 - Draw up language for an API (a code interface) for the package to expose
 - Build the adapters style framework; keep it loose for now
 - Implement a Runkeeper verison
 - Implement a Jawbone version
 - Do more great stuff from there
