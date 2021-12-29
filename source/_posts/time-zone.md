---
title: "Time Zone"
categories:
  - trivia
toc: true
date: 2019-05-08 11:24:14
tags:
  -
---

[Time zone - Wikiwand](https://www.wikiwand.com/en/Time_zone)
[Time Zone Map](https://www.timeanddate.com/time/map/)
[World_Time_Zones_Map.png (4000×2157)](https://upload.wikimedia.org/wikipedia/commons/8/88/World_Time_Zones_Map.png)

[timeanddate.com](https://www.timeanddate.com/)
[World Clock and Time Converter - Savvy Time](https://savvytime.com/)
[World Time Zone Map](https://24timezones.com/timezone-map)
[The Time Zone Converter](https://www.thetimezoneconverter.com/)
[Time Zone Converter -- Tools](http://www.timezoneconverter.com/index.php)

[UTC is Enough for Everyone, Right?](https://zachholman.com/talk/utc-is-enough-for-everyone-right)
[Strangest Time Zones of the World - YouTube](https://www.youtube.com/watch?v=uW6QqcmCfm8)
[The Problem with Time & Timezones - Computerphile - YouTube](https://www.youtube.com/watch?v=-5wpm-gesOY)

[Why Britain is the Center of the World - YouTube](https://www.youtube.com/watch?v=g52A2CPEi4A)
[The International Date Line, Explained - YouTube](https://www.youtube.com/watch?v=aBppb2quqkE)

[What is the standard way to add N seconds to datetime.time in Python? - Stack Overflow](https://stackoverflow.com/a/57498235)

```python
def add_timedelta_to_time(t, td):
    """Add a timedelta object to a time object using a dummy datetime.

    :param t: datetime.time object.
    :param td: datetime.timedelta object.

    :returns: datetime.time object, representing the result of t + td.

    NOTE: Using a gigantic td may result in an overflow. You've been
    warned.
    """
    # Create a dummy date object.
    dummy_date = date(year=100, month=1, day=1)

    # Combine the dummy date with the given time.
    dummy_datetime = datetime.combine(date=dummy_date, time=t, tzinfo=t.tzinfo)

    # Add the timedelta to the dummy datetime.
    new_datetime = dummy_datetime + td

    # Return the resulting time, including timezone information.
    return new_datetime.timetz()
```
