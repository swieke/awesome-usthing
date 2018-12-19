# EMS Specification
Finally EMS has a specification.

## Goal :checkered_flag: 

- USThing users can join the events with their created profile in app
- Event admin can organise the event easier
- Eventbrite + EventXtra

## Specs :books: 

-  Event List View
    1.  Top Banner
        -  Show Top five ranking score image (ranking score calculation see below)
        -  Show placeholder banner when no events
        -  Auto scrolling every 4 seconds and repeat indefinitely 
    2.  Events list
        -  Three tabs
            - All
            - Joined
        - Main list
            - Ranking: days from event creation date `event._create_at` + event click rate `event.clickrate` * 0.5
            - Show if `event.published` is `true`
            - Each row
                1.  Organiser image `event.organizer -> user.image`
                    - show usthing logo as placeholder
                2.  Organiser name `event.organizer -> user.organizer_name`
                    - show nothing when empty
                3.  Event image `event.organizer`
                4.  Event name `event.name`
                5.  Event time `event.beginTime event.endTime`
                    - DB Format: `yyyy-MM-dd HH:mm:ss`
                    - App Show as: dd MMM yyyy HH:mma - dd MMM yyyy HH:mma

        - Show 10 events max, auto load when scroll to the bottom
        - Empty message when no events (No Available Events, Please check again later 😙)
        - Search
            - Search the events name and organiser
- Event Detail Page
    - Organizer Image
    - Organizer Name
    - Event image 
    - Event name `event.name`
    - Event Time `same as list page`
    - Event Venue `event.venue`
    - Event Price `event.fee`
    - Event Quota `event.quota`
    - Event Description `event.description`
    - Rundown 
        - JSON Array: `[{"time": "yyyy-MM-ddTHH:mm:ss.SZ","action":"xxx"}]
    - When `event.link` & `event.join_label` is not empty, go to browser to show `event.link`. Label for the button becomes `event.join_label`
    - Attendnace Status
        - "awaiting-payment", 
        - "joined", 
        - "checked-in", 
        - "checked-out", 
        - "cancelled"

- Event Admin
    - List
        - Show all events if `event.admins` contains current user
        - Show total registratns
    - Detail Page
        - Show whole attendance list with ordering:
            - "awaiting-payment", 
            - "joined", 
            - "checked-in", 
            - "checked-out", 
            - "cancelled"
        - Click to change the attendance status
        - QR Code button to scan QR code
            - Two modes
                - Joined -> Checked-in
                - Checked-in -> Checked-out
        - Preview Events button
            - Show the events as Event Detail page
## Screenshot from iOS
- Events Main Page
![](https://i.imgur.com/vCzxsUp.png)
- Joined Events Tab
![](https://i.imgur.com/V9rlQmJ.png)
- Event Detail Page
![](https://i.imgur.com/pJiADFY.png)
- Events Admin List
![](https://i.imgur.com/7c53z9V.png)
- Attendance List
![](https://i.imgur.com/msif0US.png)

## TODO :pencil2: 




