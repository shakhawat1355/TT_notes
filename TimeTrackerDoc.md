# Nopstation Time Tracker System
Welcome to the Nopstation Time Tracker System technical documentation. This documentation's prime purpose is to help you understand how nopstation time tracking system works and how to develop features for it. 

## Introduction
Nopstation Time Tracker System is a combination of three plugins installed in nopcommerce ecommerce platform. These three plugins work together to create Nopstation Time Tracking System. Lets see how they work-

### ⚙️ Trello PowerUp Client
This plugin provides trello powerUp which is used by the users to input data like spent time log/daily standup data etc. A trello powerUp is a extension of trello to add extra functionality in trello.

💡 Functionality -
- provides a view of the custom powerup made by time tacker team.
- Post/Get Data from users to TimeTracker Plugin.
Here a diagram that illustrates the workflow-
![Sample Image](/assets/Trello%20PowerUpClientbg.png)

### ⚙️ Time Tracker Plugin
This plugin is the backbone of Time Tracker system. It holds all the entities and Api's needed. Both Weekly report plugin and Trello powerUp client plugin are directly depend on this  plugin.

💡 Functionality -
- Serves data to trello powerup client via Api responses.
- Recieves data from Trello powerup client and processes it and saves it to the database.
- holds all the entities and models needed in other plugins.

Here a diagram that illustrates the workflow-
![Sample Image](/assets/Trello%20PowerUpClientbg.png)


### ⚙️ Weekly Report
This plugin is responsible for admin view and frontend of Time tracker.The admin manages users and maps with different entities.  

💡 Functionality -
- provides data range report and daily standup report by proccessing data from db.
- Responsible for weekly report Emailing system.
Here a diagram that illustrates the workflow-
![Sample Image](/assets/Trello%20PowerUpClientbg.png)