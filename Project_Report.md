# Project Report: AI-Based Smart Study Planner 📄

## 1. Problem Statement
•	The students are facing certain difficulties while creating an efficient study plan, which is resulting in poor time management, stress, and anxiety among the students before the exams. The traditional method of creating a study plan is not efficient, as it is not flexible and does not follow the learning curve of the student. Hence, the problem needs an efficient solution, which can adapt itself according to the learning curve of the student.
## 2. Why It Matters
•	The exams, stress, and anxiety among the students are resulting in poor memory, poor mental health, and burnout. The proposed solution will help the student to plan their tasks and complete their daily tasks, which will improve their studies, reduce stress, and improve their performance.
## 3. Approach to Solving the Problem
•	I proposed a solution for the above-mentioned problem by creating a web application named “Smart Study Planner.” The proposed solution is efficient, as it is dynamic and flexible and can adapt itself according to the learning curve of the student by creating a dynamic schedule for the student. The proposed solution is based on the mathematical formulation of the problem. The proposed solution is a Greedy + Heuristic solution. The proposed solution will check all the subjects every day and generate time slots for all the subjects according to their priorities, calculated by the heuristic function. The priority of all the subjects is calculated using the following equation:

                   Priority = Difficulty x (1/Days Left)
                   
•	Where Priority is the calculated priority, Difficulty is the difficulty level, and Days Left is the days left for the exams.

•	This ensures that the student studies the subject first that is more difficult and closer to the exam.

## 4. Key Decisions Made

•	Algorithm Choice: Instead of using a pure Breadth-First Search Algorithm, which is computationally expensive due to the large schedule, I have adopted a greedy algorithm approach. This is because it is an approximation to the solution, requiring very little computation, and yielding results instantly.

•	Proportional Allocation: Instead of using all the time for the single highest-priority subject, I have adopted the proportional allocation of time for all active subjects according to their relative priority scores.

•	Built-in Constraints: Instead of allowing the algorithm to yield unrealistic results, i.e., the amount of time allocated to a subject in a day, I have adopted strict constraints on the amount of time allocated to a subject per day, e.g., 4 hours per day.

•	Cognitive Recovery: Instead of allowing the student to be on their own devices, I have adopted the approach where the algorithm forces the student to take a break every 15 minutes between sessions to adopt the Pomodoro technique for learning.

•	Revision Mode: Instead of keeping the student in the 'Study Mode' always, I have adopted the approach where if the subject is within 2 or fewer days from the exam, the mode automatically switches from 'Study Mode' to 'Revision Mode'.

•	Tech Stack: Instead of using a bloated framework, I have adopted the approach where I have used a very light technology stack, i.e., Vanilla HTML/CSS/JavaScript for the client-side and Python/Flask for the server-side. This is because it is very light, with emphasis on the algorithm and beautiful user interface.

## 5. Challenges Faced
•	Heuristic Balancing: Developing a heuristic algorithm to balance the need to study urgent, but not so important, issues and the need to study not so urgent, but the more important issues, was a bit challenging. However, after some back and forth and balancing, I managed to achieve a good balance.

•	Handling Edge Cases: For instance, in cases where there are multiple subjects to be studied and their dates are the same, the algorithm would need to be able to handle such cases. However, the algorithm was having issues fitting all the details within the one-hour limit of the day. This was resolved by incorporating the proportional allocation.

•	State Management without Frameworks: Dynamically managing the DOM elements, state management, and rendering the schedule table without the need for a reactive framework like React.

•	Integration: Ensuring proper communication between the frontend and the Python backend, especially in terms of date management and conversions, and ensuring the proper management of time zone differences using datetime.

## 6. What I Learned
•	Practical Algorithm Design: I learned how to apply the theoretical algorithm in searching and satisfaction.

•	Full Stack Development: I learned how to develop a full-stack application from scratch, integrating the Python backend API and the functional frontend.

•	API Integration: I learned how to better work with APIs, especially in terms of API interactions.

•	Third-Party Library Integration: I learned how to better work with and leverage third-party libraries, especially in terms of creating visual analytics using Chart.js and jsPDF.

•	Project Structuring: I learned the importance of structuring and separating different components of the code, especially in separating the algorithm in the scheduler.py file and the API in the app.py file.

