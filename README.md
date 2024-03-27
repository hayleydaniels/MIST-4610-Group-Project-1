# Group 1 MIST4610 Group Project (Fall 2024)

## Team Name: 
61608 Group 1

## Team Members:

1) Dylan Palenik: [@DylanPalenik1](https://github.com/dylanpalenik1)
2) Aakash Dholakia: [@AakashDholakia](https://github.com/AakashDholakia)
3) Dan Kerik: [@dan-kerik](https://github.com/dan-kerik)
4) Hayley Daniels: [@hayleydaniels](https://github.com/hayleydaniels)
5) Jordan Beal: [@JordanBeal](https://github.com/Jlb65166)
6)  Lexie-Anne Rodkey: [@LexieRodkey](https://github.com/lexierodkey)

## Problem Description:
The objective of this project is to model and develop a relational database that comprehensively covers all aspects of a soccer club’s operations. This includes Facilities, Training Sessions, Players, Managers, Squads, Matches, Sponsors, Injuries, and Player Stats. 

The database will be populated with valid sample data to reflect real-life scenarios and will be optimized for queries that help extract insights into player performance, squad efficiency, match outcomes, facility utilization, and the financial landscape of sponsorships.

By incorporating these entities and their relationships into the database, efficient management of club operations is ensured, encompassing tasks such as scheduling sessions, monitoring player participation, analyzing performance metrics, managing injuries, and facilitating sponsorship agreements. The database will serve as an informational hub for stakeholders and help the team make strategic decisions and achieve operational effectiveness within the soccer club

## Data Model:
In regards to the data model best suited for our scenario of a soccer club, twelve entities are required. These include Facilities, Training Sessions, Training Session Attendance, Manager, Players, Squad, Squad Composition, Matches, Match Sponsor, Sponsor, Injury, and Player Stats.

Starting with facilities, each facility can have multiple training sessions, and sometimes training sessions can exist without a facility, just like a facility can exist without any current training sessions. As such, having a non-identifying 1-M relationship, in this case, allows for more flexibility and independence between these entities.
In regards to training sessions, each training session can have one facility, but can also have multiple individuals in attendance at these sessions. Multiple training sessions can have multiple attendees. Therefore, an associative entity called Training Session Attendance was created. This entity links the Training Sessions with Players and Managers. This Training Session Attendance entity allows users to view who is and is not attending each training session by receiving the primary keys from the associated entities as foreign keys.

Players is a large entity related to multiple other entities. Players can attend training sessions, be part of a Squad, have multiple injuries, and play multiple matches. The relationship between Players and Training Sessions was previously mentioned as an M-M relationship with an associated entity named Training Session Attendance. The relationship between Player and Squad is also an M-M identifying relationship. Therefore, the associative entity named Squad Composition was created. Many players can play on many squads.

The relationship between Players and Matches is a M-M relationship. Multiple players can play multiple matches, and multiple matches can have multiple players. Because it is M-M, the associative entity labeled Player Stats was created. This entity contains the primary keys from Players and Matches as foreign keys.

It should also be noted that Players can receive injuries through their time in the club. Therefore the relationship between Players and Injury is 1-M. One player can obtain multiple injuries.

Squads can consist of multiple players, have one manager, and play multiple matches. Therefore there are three relationships defined in this case. These include the previously mentioned M-M relation between Players and Squad, a M-1 non-identifying relationship between Squad and Manager, and a 1-M non-identifying relationship between Squad and Matches. Each Manager can manage multiple squads, but each squad may only have one manager

<img width="692" alt="Screenshot 2024-03-26 at 5 59 51 PM" src="https://github.com/dylanpalenik1/Group-1-Mist-4610-Group-Project-1-2024/assets/164935337/ec64138e-6082-4c74-a2a9-f4c569a6b1ec">

## Data Dictionary:
<img width="600" alt="Screenshot 2024-03-26 at 6 12 19 PM" src="https://github.com/dylanpalenik1/Group-1-Mist-4610-Group-Project-1-2024/assets/164935337/591df87c-b267-4b6a-b037-0cbac6f3b11b">

<img width="602" alt="Screenshot 2024-03-26 at 6 03 18 PM" src="https://github.com/dylanpalenik1/Group-1-Mist-4610-Group-Project-1-2024/assets/164935337/3eaaa3e6-7241-4d09-a153-3613c7e63ebe">

<img width="611" alt="Screenshot 2024-03-26 at 6 13 04 PM" src="https://github.com/dylanpalenik1/Group-1-Mist-4610-Group-Project-1-2024/assets/164935337/99a081d1-1cd2-4413-95fc-0e6cd0bd4455">

<img width="605" alt="Screenshot 2024-03-26 at 6 15 49 PM" src="https://github.com/dylanpalenik1/Group-1-Mist-4610-Group-Project-1-2024/assets/164935337/42e526db-955c-4453-9e72-3e4daedf2664">

<img width="604" alt="Screenshot 2024-03-26 at 6 22 38 PM" src="https://github.com/dylanpalenik1/Group-1-Mist-4610-Group-Project-1-2024/assets/164935337/a56e0835-c743-4f07-85a3-372d3208e31c">

<img width="603" alt="Screenshot 2024-03-26 at 6 22 56 PM" src="https://github.com/dylanpalenik1/Group-1-Mist-4610-Group-Project-1-2024/assets/164935337/ea0d0618-d920-4d8c-b6d6-f2b644169fc1">

<img width="601" alt="Screenshot 2024-03-26 at 6 21 41 PM" src="https://github.com/dylanpalenik1/Group-1-Mist-4610-Group-Project-1-2024/assets/164935337/dae26cc6-917a-4c81-a8c6-13ca5f9d4e55">

<img width="592" alt="Screenshot 2024-03-26 at 6 20 59 PM" src="https://github.com/dylanpalenik1/Group-1-Mist-4610-Group-Project-1-2024/assets/164935337/d1bc0a07-f991-4672-a55e-5a45e5a5da63">

<img width="614" alt="Screenshot 2024-03-26 at 6 16 20 PM" src="https://github.com/dylanpalenik1/Group-1-Mist-4610-Group-Project-1-2024/assets/164935337/527577fc-a64d-4026-836b-aa9c9e191832">

<img width="602" alt="Screenshot 2024-03-26 at 6 16 52 PM" src="https://github.com/dylanpalenik1/Group-1-Mist-4610-Group-Project-1-2024/assets/164935337/e8bc16ae-3dbb-40c7-938a-78e94b413509">

<img width="597" alt="Screenshot 2024-03-26 at 6 22 01 PM" src="https://github.com/dylanpalenik1/Group-1-Mist-4610-Group-Project-1-2024/assets/164935337/137d7480-6ea1-44a1-8c8d-193c1e5991b6">

<img width="598" alt="Screenshot 2024-03-26 at 6 21 20 PM" src="https://github.com/dylanpalenik1/Group-1-Mist-4610-Group-Project-1-2024/assets/164935337/ca497fe5-3203-494f-a607-bfab8a784e55">

<img width="607" alt="Screenshot 2024-03-26 at 6 17 58 PM" src="https://github.com/dylanpalenik1/Group-1-Mist-4610-Group-Project-1-2024/assets/164935337/7194a096-74b7-433c-ad7e-d9ed9e253820">

## Queries:
<img width="630" alt="image" src="https://github.com/dylanpalenik1/Group-1-Mist-4610-Group-Project-1-2024/assets/164935337/a2248bb0-5bab-45e8-aa47-810318e58a9c">

<img width="567" alt="Screenshot 2024-03-27 at 4 13 51 PM" src="https://github.com/dylanpalenik1/Group-1-Mist-4610-Group-Project-1-2024/assets/164935337/59c6b23a-4d75-4b09-8e2e-bbfb27b61839">

<img width="562" alt="Screenshot 2024-03-27 at 4 14 00 PM" src="https://github.com/dylanpalenik1/Group-1-Mist-4610-Group-Project-1-2024/assets/164935337/f30b2a2a-7cdd-473b-8ea3-27d3fe870e54">

<img width="564" alt="Screenshot 2024-03-27 at 4 14 07 PM" src="https://github.com/dylanpalenik1/Group-1-Mist-4610-Group-Project-1-2024/assets/164935337/28c439e6-6052-4974-824b-0a2ee4ac6743">

<img width="551" alt="Screenshot 2024-03-27 at 4 14 15 PM" src="https://github.com/dylanpalenik1/Group-1-Mist-4610-Group-Project-1-2024/assets/164935337/6083f6f0-8b52-4209-a701-a957a24d85fa">

<img width="573" alt="Screenshot 2024-03-27 at 4 16 49 PM" src="https://github.com/dylanpalenik1/Group-1-Mist-4610-Group-Project-1-2024/assets/164935337/f0847b1f-227b-41ca-9cb7-06dc9bb9ede2">

<img width="546" alt="Screenshot 2024-03-27 at 4 16 59 PM" src="https://github.com/dylanpalenik1/Group-1-Mist-4610-Group-Project-1-2024/assets/164935337/8a4adbe3-9a6a-4238-8ccd-f8a556229d2e">

<img width="556" alt="Screenshot 2024-03-27 at 4 17 07 PM" src="https://github.com/dylanpalenik1/Group-1-Mist-4610-Group-Project-1-2024/assets/164935337/e838e4f6-2161-40db-8bf9-b94749c00072">

<img width="554" alt="Screenshot 2024-03-27 at 4 17 15 PM" src="https://github.com/dylanpalenik1/Group-1-Mist-4610-Group-Project-1-2024/assets/164935337/7ee11f55-b5b4-45ec-9d5e-30e80f58b4fe">

<img width="540" alt="Screenshot 2024-03-27 at 4 17 23 PM" src="https://github.com/dylanpalenik1/Group-1-Mist-4610-Group-Project-1-2024/assets/164935337/24d86270-6c1e-44f8-9a8d-22dc3a5e4504">

<img width="536" alt="Screenshot 2024-03-27 at 4 17 35 PM" src="https://github.com/dylanpalenik1/Group-1-Mist-4610-Group-Project-1-2024/assets/164935337/4839d4a6-0692-4d8d-9c49-aef745e1f000">

## Database information:

Name of the database: ns_Sp24_61608_Group1

Additional Information: Each query above is in the database using stored procedures which can be called upon using the following format: CALL TP_Q1();
