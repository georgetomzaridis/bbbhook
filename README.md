<p align="center">
<img src="https://raw.githubusercontent.com/georgetomzaridis/bbbhook-bigbluebutton/main/bbbhook-sh1.png" alt="BBBHook WebGUI"
</p>
  
## BBBHook

BBBHook is a automated mechanism programm, that communicates with Big Blue Button and tracks user time consumption in every session:
- Monitoring every session using Big Blue Button WebHooks
- Tracking when users join/leave the session
- Display Analytics using Moodle LMS Toolbox Intergration (using external tools)
- Dynamic Search / Deep dive in the recorded data using search filters (From Date, To Date, Fullname etc)
- Export the data in PDF Files

## Disclaimer / Project Notes
- The data are randomly generated for the <ins>**demo/introduction purposes only!**</ins> They have absolute <ins>**no connection with real-life data**</ins> (user personal infromation, time data etc). If some names exists in real-life, again have <ins>**no connection**</ins> at all with this project/platform/dataset.
- This repository for this project have <ins>**no available source code**</ins> because is <ins>**available only for a specific company usage and not for the public.</ins>** I will describe the technology stack and how it works below.

## Technology Stack
 - Laravel (PHP MVC Framework) [Back-end]: https://laravel.com/
 - MariaDB [Data storage]: https://mariadb.com/
 - Redis [Session/Caching]: https://redis.io/
 - Big Blue Button WebHook [Sessions/Events]: https://docs.bigbluebutton.org/dev/webhooks.html
 
## Architecture Explained
<img src="https://raw.githubusercontent.com/georgetomzaridis/bbbhook-bigbluebutton/main/bbbhook-architecture-explained-diagram.png" alt="Architecture Explained">

1) Users join sessions
2) Big Blue Button send events in the BBBHook API using WebHook (joins, leaves, connections, user information etc)
3) BBBHook API Filters and Process the wanted data
4) Storing the correct data in specific format in the database
5) Admins request access to data analytics from Moodle LMS
6) BBBHook API authenticate and authorize Moodle LMS Platform and User (checking valid license, user tokens etc)
7) Display the data analytics inside the Moodle LMS

## Project Images
User Statistics (WebGUI)
<img src="https://raw.githubusercontent.com/georgetomzaridis/bbbhook-bigbluebutton/main/bbbhook-sh2.png" alt="User Statistics (WEBGUI)">

Exported Data in PDF File
<img src="https://raw.githubusercontent.com/georgetomzaridis/bbbhook-bigbluebutton/main/bbbhook-sh3.png" alt="Exported Data in PDF File">

Access from Moodle LMS
<img src="https://raw.githubusercontent.com/georgetomzaridis/bbbhook-bigbluebutton/main/bbbhook-sh4.png" alt="Access from Moodle LMS">

## Questions/New Ideas?

- If you have any questions dont hesitate to contact me: georgetomzaridis@gmail.com.
- You got an idea? I am happy to hear it! Submit it freely!
