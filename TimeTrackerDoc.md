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
<img src="assets/Trello%20PowerUpClientbg.png" alt="Description" width="400" height="200" />
### ⚙️ Time Tracker Plugin
This plugin is the backbone of Time Tracker system. It holds all the entities and Api's needed. Both Weekly report plugin and Trello powerUp client plugin are directly depend on this  plugin.

💡 Functionality -
- Serves data to trello powerup client via Api responses.
- Recieves data from Trello powerup client and processes it and saves it to the database.
- holds all the entities and models needed in other plugins.

Here a diagram that illustrates the workflow-

<img src="assets/tt_workflow.png" alt="Description" width="300" height="200" />

### ⚙️ Weekly Report
This plugin is responsible for admin view and frontend of Time tracker.The admin manages users and maps with different entities.  

💡 Functionality -
- provides data range report and daily standup report by proccessing data from db.
- Responsible for weekly report Emailing system.
Here a diagram that illustrates the workflow-

<img src="assets/weeklyReport.drawio.png" alt="Description" width="300" height="200" />


So if we add all the plugins the workflow will look like-

<img src="assets/Total.jpg " alt="Description" width="300" height="200" />


## How to Delevop feature in Time tracker
First of all to develop any feature you will need a complete idea of how nop plugins function.

### 🔧 Trello Powerup Client Plugin
- To develop any feature in Trello powerUp client plugin you will need to know about 
[Trello powerup client library](https://developer.atlassian.com/cloud/trello/power-ups/ )
- the whole plugin depends on ajax request handled by time tracker plugin. so to post/get any data you will have to create api endpoints in time tracker plugin along with entities/models/factories/service etc.

### 🔧 Time Tracker Plugin
- Its actually very easy to add any API  endpoints here. Just copy an existing API endpoint and modify it as per requirement.
- Any entity or domain you need must be created on this plugin.

### 🔧 Weekly Report Plugin
- this plugin has two parts one in the public site and another in the admin area. So any feature you need to develop should be based of area either public or admin area.
- In the admin area, adding a feature is quite simple as goes by the book.
- But in the public site there are two main features "Date Range Report" and "Daily Standup Report". To add anything in these views you will need to work on their js files. They JS files may seem complex and hard to understand as the dont belong to default nop views. So take time and try to understand how things work.

Hope this doc has helped you understand how Nop Time Tracker works and how to develop features in this system.
