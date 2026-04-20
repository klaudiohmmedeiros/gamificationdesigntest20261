# Gamification Design for a Software Testing course

This page offers a more complete guide to the gamification design proposed in our submitted work.

## About the spreadsheets

Initially, this gamification design will be implemented through spreadsheets. 

A template for the spreadsheet mentioned in the study, for visualization purposes, can be found here: [Class spreadsheets - Example 1.pdf](https://github.com/user-attachments/files/26869138/Class.spreadsheets.-.Example.1.pdf). The game information is in another spreadsheet. This spreadsheet, for visualization purposes, can be found here: [Class spreadsheets - General.pdf](https://github.com/user-attachments/files/26869217/Class.spreadsheets.-.General.pdf).

These spreadsheets exchange information with each other. For example, when we change the student's username in their spreadsheet, their name automatically changes in the general information spreadsheet and leaderboards. When the leaderboard change in general information spreadsheet, the updated leaderboard is submitted to each student's spreadsheet.

## Spreadsheet information

For each student, the spreadsheet has the following informations:

- **Name (or nickname)**: The name of the student. You can give the option for the student to use a nickname for the gamified dynamic;
- **Student's team**: The team that the student is part of;
- **Points**: This score is calculated based on the sum of all missions the student has completed, based on the marking of checkboxes related to each mission;
- **Progress**: A green progress bar that fills when the student complete a mission. The bar's fill level is proportional to the number of points the student has compared to the maximum possible score;
- **Average points**: The average score of all students in the gamified dynamic;
- **Level**: The level of the student. The level is represented by stars, where 1 star means 1 level. Each level has a point limit value that, when the student reaches this value, they advance to the next level. The number of points needed for the student to level up is increased as they reach higher levels;
- **Next level**: The amount of points needed for the student to reach the next level;
- **Student leaderboard**: The top students ranked based on the accumulated points. Ideally, the leaderboard doesn't show all students to not demotivate students behind its peers, but the instructor can decide if they want to show some students or all students;
- **Team leaderboard**: The teams ranked based on the accumulated points obtained by its members;
- **Checklist**: Each mission has a corresponding checklist. When the student completes a mission, the instructor can mark the mission as completed by checking the checkbox;
- **Mission**: The name of the mission. The instructor can use their creativity to create new missions;
- **Description**: The description of the mission, that explains what the student must do to complete the mission;
- **Reward**: The number of points associated with the mission. When the instructor marks a mission as completed, its reward is added to the number of points obtained by the student;

The "General" page has the following informations:

- **Students' Information**: A list with each student's name and points. These information come from the student's spreadsheet;
- **Students' Information (ranked)**: The same list above but sorted by points obtained;
- **Team leaderboard**: A list with each team in the gamified dynamic;
- **Team leaderboard (ranked)**: The same list above but sorted by points obtained by the team;
- **Points needed for level**: How many points do the student need for reaching certain levels in the gamified dynamic. It's also used for calculate how many points the student need for level up (for example, if the player needs 150 points to reach level 2 and have 100 points, they need 50 points to level up);
- **General information**: Additional information about the gamified dynamic:
    - **Average students' points**: The arithmetic mean of the sum of points obtained by all students in the gamified dynamic divided by the number of students;
    - **Max possible points**: The maximum number of points that the student can earn in the gamified dynamic. It's important to calculate, for example, the progress of the student represented by the progress bar;
    - **Number of students**: The number of students participating in the gamified dynamic. It's important to calculate, for example, the average points of the class;


## Mission ideas

- **Attendance missions**: Missions based on attendance of the student in classes. It's recommended to allow a certain tolerance for absences per assessment unit (e.g. *"The student has 90% of attendance on Unit I"*, *"The student has one or less absences on Unit I"*);
- **Grading missions**: Missions based on grading of the student in assessment units. The value thresholds may vary based on the scoring system used in the institution (e.g. numeric grades, concepts). It's recommended to allow a certain tolerance for grading per assessment unit (e.g. *"The student got a grade of 86 or more in Unit I (max 100)"*, *"The student got a A grade in Unit I"*);
- **Exposition missions**: Missions based on participation on in-class or online discussions. They can represent in-class presentations or other types of tasks where students present something for the class or instructor (e.g. *"The student participated in 3 or more online discussions"*, *"The student presented the results of their research about Software Bugs and Their Consequences to the class"*);
- **Team missions**: Missions based on teamwork. They can represent missions for tasks where each student has a different subtask to do or scoring goals for the team (e.g. *"The student's team scored over 1000 points*", *"The student did a static analysis of the source code of Example project"* where another member has *"The student did the refactoring of the Example source code"*);
- **Exercise missions**: Missions based on exercises done by students over the time. It can be based on the count of exercises done (e.g. *"The student completed 5 or more exercises of the Exercises page"*, *"The student completed 10 or more exercises of the Exercises page"*);
- **Specific missions**: Missions based on specific actions for exercises or other actions throughout the gamified dynamic. Here as tips for these missions, based on Software Testing curriculum:
    - **Complete specific exercises**: The mission is completed when the student completes an exercise. The instructor may define their criteria for exercise completion;
    - **Founding different kinds of problems**: These problems may be faults or defects. In the exercise, the student can be asked if each of these problems are faults or defects, for example (e.g. *"The student got 90% of right answers for the "Is This A Fault or a Defect" quiz"*);
    - **Founding different kinds of bugs**: The mission is completed when the student finds a minimum number of different bugs in an exercise or system (e.g. *"The student found 6+ different bugs on the "Library's Rent System" source code"*);
    - **Write unit tests**: This mission is completed when the student implement unit tests for a problem given by the instructor (e.g. *"The student created and submitted unit tests for the "Library's Rent System" source code"*, *"The student used 6 or more different @ (tags) of JUnit 5 for unit tests of "Library's Rent System" source code"*);
    - **Code coverage**: This mission is completed when the student uses tests to cover a certain percentage of the code given in a problem. These can be verified with tools like EclEmma (e.g. *"The student got a code coverage of 80% or more for the "Library's Rent System" source code"*);
    - **Equivalence classes**: This mission is completed when the students use Equivalence Partitioning on a testing problem (e.g. *"The student identified half of the equivalence classes for the "Library's Rent System" source code correctly"*, *"The student identified all equivalence classes for the "Library's Rent System" source code correctly"*, *"The student have created test cases for each equivalence class for the "Library's Rent System"*);
    - **Boundary value analysis**: This mission is completed when the students use boundary value analysis on a testing problem (e.g. *"The student identified critical boundary values and created test cases that target "Library's Rent System" vulnerable points"*);
    - **Structural testing**: This mission is completed when the student use structural testing for a task (e.g. *"The student explored the internal structure of "Library's Rent System" and designed test cases that exercise half of its logic paths"*, *"The student explored the internal structure of "Library's Rent System" and designed test cases that exercise all of its logic paths"*);
    - **Refactoring**: This mission is completed when the students use refactoring on a code (or codes) preserving the results of previous tests (e.g. *"The student has found 3 code smells in "Library's Rent System" source code"*, *"The student applied 5 refactoring techniques in "Library's Rent System" source code without chaning its behavior"*, *"The student reduced the cyclomatic complexity of "Library's Rent System" source code"*);
    - **Regression testing**: This mission is completed when the students successfully use regression testing to detect bugs (e.g. *"The student changed the rent penalty calculation without breaking other functions of "Library's Rent System""*, *"The student identified and fixed the function that breaks the regression tests of "Library's Rent System"*); 

 




