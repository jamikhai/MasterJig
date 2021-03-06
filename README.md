# MasterJig

In collaboration with Fox Imler: https://github.com/foximler

Taking ice fishing to the future.

1. Inspiration:
  After going ice fishing for the first time at the start of 2020, I noticed a problem that nobody seemed to think twice about. Often, when ice fishing, devices known as tip-ups are used. They are mechanical systems that hold a line in an ice fishing hole, and release a small flag when pulled by a fish. Although very common, I saw a lot of potential for a digital solution. These tip-ups could not be seen from very far (such as from inside a tent or cabin), and could not been seen at night (in northern Alberta, it gets dark before 5pm in Winter).
  
  
2. Our System:
  Our end goal was to ultimately have an easy way to monitor our tip-ups by having an electronic notifcation and status system. First, a Raspberry Pi (RP) was used as our prototype unit connected to a pressure switch, activated by the pull of a string. The RP connected to a Flask API to communicate sensor data (like temperature and location), as well as switch data to know if a fish pulled on the line. Once parsed by our API, the data was saved in an SQLite3 database and if the switch was triggered, an email/text notification was sent out. A small front-end of a website was then built to monitor the tip-ups using information in the database.
  
 
3. Improvements:
  The system works with our one test RP and sensor, and can be monitored from the Flask website, which can be buitl upon for more features. We have support for multiple tip-ups per user and the ability to add to the database at any time. The Flask API is expandable and can support a large amount of users in the future. Winterized and refined sensors can evetually be created for real use on a frozen lake.
