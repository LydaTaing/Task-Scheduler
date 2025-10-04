# Task Scheduler


## Importance and Motivation 
This particular project is important to us because as students ourselves, the idea of being organized on the various activities, homework, and tests dates are essential to doing well in school. Working on this project closely aligns to our own necessities are students, which we can therefore utilized in our personal lives in the future. As we are implementing different categories of tasks, this project can be personalized to an individual. 

## Tool and Technologies: 
* C++ (terminal base for interface) 

## input/output
* Input: title, description, classification, date, priority, duration
* Output: Lists of tasks to complete in order, suggested schedules

## Feature
### Overview 
This application allows users to create and manage tasks efficiently. Users can create tasks with attributes such as title, description, classification, priority, duration, and due date. Optional fields are also available to enhance flexibility. Additionally, users can create task lists, grouping multiple tasks together to represent larger projects with subtasks.

Users can display, edit, delete, and undo operations on tasks and task lists. The application provides sorting features based on different criteria and can suggest a schedule based on the user's current tasks. 

### Core Features
* Manage daily tasks and set up reminders
* Create subtasks for tasks
* Sort by deadline (tasks with the sooner due dates appear higher)
* Edit/Delete/Sort tasks
* Add tags to categorize tasks (e.g., "Science Class," "Math Homework")
* Optional 

#### Additional Feature:
 * Assign specific time slots for tasks in a daily schedule
 * Linked Tasks (Once one task is completed, another task is assigned)
  

## User Interface Specification
The Task Scheduler application provides a structured flow for managing events and tasks efficiently. The navigation diagram illustrates how users can interact with the system from the Home Screen and perform various actions on tasks.

### Navigation Diagram
<img width="1045" alt="Screenshot 2025-02-27 at 2 41 08 AM" src="https://github.com/user-attachments/assets/0c8d16a6-fd24-4a4b-9f24-4e9969e4e27c" />


### Screen Layouts
<img width="771" alt="AD_4nXd3yY746di-W9LHkeTGwQUy514UbkJWhY2GCx1RH1O8RoGhUZintlI3sRf-Iws1649zHmfcOweQUFPd5lraz3D9h1j_NpERTWdXq2T1OdYcW-c2Xt2lGCcqIGhGLZ-XK5qkCLhfAQ" src="https://github.com/user-attachments/assets/2679e73f-8121-488c-aa28-b43ee020188e" />

The main menu has two options: create new event, view current schedule or view completed task. Users can also end the program directly by entering 0. 

<img width="771" alt="AD_4nXfMvfk03_GZPOxSOCHx6xax7g_Ot4UBsBcbNDTiZ8J1T9MBarAwNyLakMdklw-mBNm8uSVKxZMgDVFAV9CbgabhmqtrtlnWh51fM9lzgntG3oW-A--OyFbcP5-zvA_ZcI9fFkVI" src="https://github.com/user-attachments/assets/e12dbe04-f91a-4311-9425-db1a5f5495a3" />

If the user selects 1, the program will ask the user for the new event title, time, priority and category. After creating the new event, the user can view the current schedule, create a new event or go to the main menu. 

<img width="771" alt="IMG_6663" src="https://github.com/user-attachments/assets/b7ab4d27-9058-48d9-9ab7-760456cca647" />

If the user selects 2, the program will arrange the current events by category or by priority. The user can select a specific event and edit it. The user can edit the event title, time, delete it or mark it as complete. 
After the user selects a task, the program would ask how the user wants to edit the event. 

<img width="771" alt="IMG_8861" src="https://github.com/user-attachments/assets/582264f6-1e17-4bbe-a55f-f630ee87a98c" />

User can choose to link event or make adjustment on the event inoformation and option to return main menu. 

<img width="771" alt="IMG_0379" src="https://github.com/user-attachments/assets/c4e6f579-0774-419b-8a42-88faafa57184" />

If the user selects Link events, the user can link the current event to another event. After that, user can link another event or return to previous menu. 
After any edit completed, the program will ask the user whether they want to create a new task or return to the main menu. 

<img width="771" alt="image" src="https://github.com/user-attachments/assets/fe367bbf-b25d-4b0e-808a-8d3b1a733eb1" />

If the user selects 3 from the main menu, the completed task would be displayed. User can choose display by time or by priority. After the completed tasks are displayed, user would return to the main menu. 

## Class Diagram
Data class: This class is responsible for tracking the user’s task statistics related to their productivity levels. The getters and setters will store the user’s average time completion for each task, total task completed, and how many pending tasks they have left.

Schedule class: This class is responsible for tracking how many tasks we can add or remove, the priority level, the name of the schedule, the display, and the duration it will take to complete and whether the schedule is active or inactive.

Task class: This class is responsible for keeping track of the name of the task, priority level, what the task is for, the progress of the task, and whether it is a recurring task or not.

Notification class: This class is responsible for the message the user will receive, the way it is displayed, if the user wants the notification to reappear, and the priority level.

Display Menu class: This class is responsible for keeping track of the selected task number and the display.

User class: This class stores the essential information regarding the name of the user and their ID number. 
![UML](https://github.com/user-attachments/assets/10db852b-30b3-433b-9545-8b6d549bde6d)




 ## Class Diagram Updated 
 ![IMG_0618](https://github.com/user-attachments/assets/0397424f-23c2-4433-82a7-b57d20b470d4)


Deleting notification class: We removed the notification class feature because we wanted to maintain a more 
Clean and efficient codebase. Therefore, we wanted to simplify our feature. This change will streamline the
code and ensure that future updates are easier to implement and maintain. 

Deleting data class: We removed the data class because there is no need for these data features and 
Functions. The idea of getting data from task is already similar to the schedule class. Therefore, removing
This class will follow the single responsibility principle. 

Deleting user class: SInce it is input, terminal-based there is no need for the user class. This is because all of
The inputs and user’s schedules will start from the display menu. Therefore, this removal encourages code
efficiency and simplicity.

Moving functions: We moved the display_categorized() function that initially belonged to the Schedule class
into the DisplayMenu class instead. This is because this function aligns better with the purpose of the 
DisplayMenu class instead of the Schedule class. By moving this into DisplayMenu class we are following
The Single Responsibility Rule where a class should have a single purpose only and not have many purposes.
We deleted the display_full() class in the Schedule class because it was repetitive to what DiplayMenu class’
displaySchedule() had already did

## Class Diagram updated 
![UML diagram](https://github.com/user-attachments/assets/5e7e357d-4ae1-4f50-996f-df369a5c720f)

* Deleted Category class and make it a part of Task in order to minimize classes in the project. 
* Adding SubTask for additional feature for user to add sub task in each task. 
* Reconstruct Schedule class into to separate classes : EventManager and EventSearch. Adds ability to search event through different variables, and marking events as complete / sort them. Each of the class create smaller scope of resposibilty and more manageable. 

## Current and Future Development 
* Current/ incomplete development : Linked Task - still in progress. Linked tasks implementation is used so that when we open a task, another one closes. We created a class to handle linked feature, but we are not able to adjust the rest of the file and tested it. Therefore, we decided to keep it out of the program for time being. 
* Future development : Sort by deadline - we didn't have a chance to work on this feature, but we keep this as a future development plan.
* Repository clean up - discard files that are no longer needed. 
 
 ## Screenshots
1. Gets user input task and subtask.
<img width="852" alt="IMG_5824" src="https://github.com/user-attachments/assets/c9f640c8-5d31-4308-b53e-309c0d652bd3" />

2. Displays all the events including subtask
<img width="852" alt="IMG_3745" src="https://github.com/user-attachments/assets/d1fe8304-ff86-41a5-a095-159417f02c7f" />

3. Edit menu output
<img width="852" alt="IMG_2064" src="https://github.com/user-attachments/assets/c3388ee5-5f9f-46c6-9fea-0a2f5a44f966" />

5. Display completed events
<img width="852" alt="IMG_9811" src="https://github.com/user-attachments/assets/616ab5e7-7959-48d6-8cc2-6668e785448f" />

6. Remove a task so that it does not show up when all events are displayed
 <img width="852" alt="IMG_2212" src="https://github.com/user-attachments/assets/0e25b6f2-cb5d-4ca1-9d5e-dc5ae233d8ad" />

 ## Installation/Usage
### Requirement:
* C++ compiler
* Google test
### Installation:
* Clone repository
* run " cmake ." and "make", then run the application with ./run
### Usage:
* User will input base on the given prompt. 
  
 ## Testing
Our project was tested by our unit tests that cover our core functions such as creating, deleting, and updating tasks. For memory checking, we used Valgrind to ensure it ran MEMCHECK-CLEAN. Our program is terminal-based where we ask the user for input. We created prompts for user input so the user can create their task and manage the app effectively. We also manually tested for error handling to ensure validity of project. 

