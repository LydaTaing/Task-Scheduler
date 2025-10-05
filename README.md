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


## Class Diagram

![UML diagram](https://github.com/user-attachments/assets/5e7e357d-4ae1-4f50-996f-df369a5c720f)

## Current and Future Development 
* Current/ incomplete development : Linked Task - still in progress. Linked tasks implementation is used so that when we open a task, another one closes. We created a class to handle linked feature, but we are not able to adjust the rest of the file and tested it. Therefore, we decided to keep it out of the program for time being. 
* Future development : Sort by deadline - we didn't have a chance to work on this feature, but we keep this as a future development plan.
* Repository clean up - discard files that are no longer needed. 
 

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

