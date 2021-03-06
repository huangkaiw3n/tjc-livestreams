TJC Streams
======================
A single page static site built with Jekyll to list available TJC livestreams
View the Jekyll docs [here](https://jekyllrb.com/docs/)

# Want to add a stream?
Streams are all defined under [\_data/streams.yml] (https://github.com/huangkaiw3n/tjc-livestreams/blob/gh-pages/_data/streams.yml)

Simply follow the format of a stream there and add on to the file by creating a PR, OR create a new issue with the stream information and I'll add it in.


# Contribute

If you have some web design skills and would like to add features and improve the design, feel free to!

## Ideas
### Right now, Simple version
Minimal data parsing version

Streams
- display_name (eg. TJC Adam Singapore Livestream)
- url (string)
- languages ([string]) eg. “English”, “Chinese”
- when_description (string) eg. “Sat 10am and 2pm (UTC +8, SGT)”


### Maybe in the future, Complicated version
With fine grained data and proper iso time data for parsing to enable features like search and filtering.

To enable search and filter like:
1. Know viewer’s time zones and filter streams that are airing now
2. Filter country
3. Filter languages

Streams
- church_name (string) eg. Adam
- country (string) eg. Singapore
- timeslots ([Timeslot])
- url (string)
- language ([string]) eg. “English”, “Chinese”


Timeslot
- day of week (ISO day of week) 1...7 eg. 6 for Saturday
- start_time (HH:mm) 0...23 Hours 0…59 Minutes eg. 14:00
- end_time (HH:mm) 0...23 Hours 0…59 Minutes eg. 16:00
- timezone (Z) Offset from UTC as +-HH:mm eg. +08:00

