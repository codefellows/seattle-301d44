![CF](https://i.imgur.com/7v5ASc8.png)
# Code 301: Intermediate Software Development

Feel free to open issues as a way to report bugs, recommend updates, and propose minor fixes.

When making branches, follow the convention of `name/feature`.

---

- [Course Overview & Objectives](#courseoverview)
- [Daily Lecture Structure](#lectures)
- [Weekly Overviews](#weeklyoverviews)
- [Course Materials in this Repository](#materials)
- [Course Operations](#operations)
- [Course GitHub Organization & Setup](#organization)
- [Course Grading & Prework; Other Academic Information](#grading)
- [Student Setup & Lab Workflow](#studentsetup)

<a id="courseoverview"></a>
## Course Overview

This course guides students through the collaborative process of creating dynamic web applications, focusing on the front end and back end independently, then creating full-stack applications.

The lab assignments for the course are in five main parts:

1. Building several client-side applications, including a personal portfolio.

1. Building a back end to consume several third-party APIs and communicate with a static front end.

1. A stand-alone mobile-only application during week 3. Students will work with the same partner throughout the week on a Heroku-deployed application. This one-week sprint will help prepare students for project week and serve as an additional personal portfolio piece.

1. Fulfillment of lab requirements via pair programming. These assignments are also a foundation for tackling technical challenges, developing code-reading skills, and gaining knowledge of application architecture.

1. Daily coding challenges which focus primarily on regular expressions, string methods, array methods, and working with objects. Students will pseudocode their solution on the whiteboard and add their final solution to a personal repository. This assignment will allow 301 students to gain practice solving coding puzzles and feel comfortable discussing code on a whiteboard. 

##### Course Learning Objectives

At the end of this course, students will be able to:
1. Collaboratively design and create single-page web applications from scratch using MVC architecture built with professional-grade HTML, CSS, and JavaScript.
1. Design dynamic frontend and backend applications which can function together or independently and are deployed to cloud platforms.
1. Explain the fundamentals of how the world-wide web works, over the internet.
1. Utilize dependency management techniques to build with third-party libraries such as ExpressJS, jQuery, and Handlebars.
1. Persist one-to-many relational data across two tables in a SQL database, sourced from third-party APIs, user-generated content, or loaded from the filesystem. 
1. Follow agile software development practices during week-long sprints, including pair-programming, stand-ups, daily retrospectives, project management with Kanban boards, regular refactoring, and working in a shared code base.
1. Enroll in a Code 401 course or attain an entry-level website development job or internship by completing the course requirements.

[-top-](#top)

---

<a id="lectures"></a>
## Daily Lecture Structure

Daily lectures typically follow a three-part pattern: code review of the previous class's lab, introduction/demo of new material, and preparation for the daily lab assignment.

##### Code Review

Ask for volunteers or select a student or pair of students for code review. You will act as the navigator while walking through the previous classs assignment(s). This portion of lecture should facilitate a discussion-based code review that is inviting and engaging, in order to promote class participation. This will allow students to vocalize on-screen code and improve their development vocabulary.

Students will often have detailed technical questions about the previous class’s assignments, so be sure to familiarize yourself with the lab requirements regularly. A typical code review lasts around 30 minutes, but can go much longer. It may be necessary to do upwards of 60-90 minutes of code review if the students are not comprehending the previously assigned lab materials.

##### Introduction and Demonstration of New Material

The subsequent portion of lecture should be focused on the introduction of new concepts. Students learn in a variety of different ways, so use a variety of delivery techniques and continue to encourage class participation by frequently checking for understanding and reiterating concepts as needed. A real-life story based on your relevant experiences may benefit the class here as well.

If the students seem eager to take a deeper dive into any given topic, feel free to perform live code demos, documentation reviews, and whiteboard diagrams as needed. Alternatively, these additions can be reserved for the end of the lecture as a part of preparing students for their next assignment.

##### Preparation for Lab

Properly preparing students for their daily assignments is a vital part of every day. To get started, open up the daily lab requirements and be sure to read through each task description and paraphrase or discuss any confusing terminology. Ask students to brainstorm potential solutions. This can be done individually, with a nearby classmate, or as a group discussion. Depending on the number of technical requirements, you can also feel free to work through one (or more) of them in class. This process should generally take around 30-45 minutes, but feel free to spend as much time as needed.

Using the concepts and class structure summarized above, you will be ready to prepare students for the next 401 course or for a job in their career. Be patient, inviting, and passionate throughout the length of your course and it will be a big boost to your overall success. Have fun!

[-top-](#top)

---

<a id="weeklyoverviews"></a>
## Weekly Overviews

### Module 1: The Front End (Classes 1-5)

***The focus of the first five classes is to introduce students to ES6 features and advance their client-side CSS skills. Students will also expand their JavaScript skills through the use of the jQuery library.***

This module will begin in class 1 with an introduction to ES6 topics including let, const, arrow functions, state, and a deeper dive into scope and prototypcal inheritance. Class 2 focuses on SMACSS, float-based layout, jQuery selectors and events. Class 3 focuses on Flexbox, templating with the [HandlebarsJS library](http://handlebarsjs.com), and a continued discussion of jQuery events. Class 4 focuses on responsive web design, icon fonts, grid-based layout, and regular expresssions. Students will build a personal portfolio page as the lab 4 assignment, which they will deploy on Heroku in workshop style during lecture 5. Students will be provided a basic `server.js` file, so this is an opportunity for a high-level discusssion of servers and their role in the Heroku deployment process. This will also give students some topics to think about as they prepare to transition into working in the back end in the next module. The portfolio page will be revisited in class 10 when students make a proxied request to the GitHub API and return their personal repositories to be displayed on their portfolio page.

### Module 2: The Back End (Classes 6-10)

***The focus of these next five classes is on teaching students how to write a backend through the use of Node.js, how to request data from third-party APIs through the use of Superagent, and how to presist data in a database through the use of SQL and PostgreSQL.***

This module will begin with a discussion about the back end, including Node.js, Express, npm, Superagent, and Postman. Data will then be persisted in a relational database. Students will also learn about the web request-response cycle (WRRC), as discussed throughout the week. Class 6 focuses on how to write a `server.js` file and how to format a request to a third-party API using Postman. As the week progresses, students will request data from additional APIs in classes 7 through 9, aggregating the responses into a single object to pass back to a static front end. Students will have access to the code base for this front end and will be able to identify the data which the front end is expecting. This will allow students to separate the front end from the back end, while creating the necessary connections between the two. Classes 8 and 9 focus on persistence in a database. Class 10 will bring the personal porfolio projects full circle. Students will be asked to request data from the GitHub API and will send data about their repositories to the front end code that was written in lab 4 and deployed in class 5. Throughout this module, students will also learn about functional programming methods including .filter(), .map(), and .reduce().

### Module 3: Full-Stack Applications (Classes 11-15)

***The focus of these final five classes is the creation of a full-stack application using [EJS](http://ejs.co/) for server-side templating. Students will create a book collection, which will eventually include the ability for a user to search for a book by title or author and receive search results from the Google Books API. Students will be able to read and create resources, with exposure to updating and deleting resources in class 14. The module will conclude with a kickoff to final projects.***

Throughout this module, students will work with a partner to build a full-stack book application. Class 11 will focus on a GET request for all resources from a student-seeded database. These resources will be displayed to the user through the use of sever-side templating. Class 12 will focus on selecting a single resource from the list and viewing the details in a new view. Class 13 will focus on building an HTML5 form with method and action attributes so users can manually enter a new resource, which will be added to the database. Class 14 will focus on adding the ability to search by title or author and initiate a request to the Google Books API. The first ten results will be displayed to the user and, through the use of a hidden form, the user can select a single book to be added to the database. Class 15 is for review and the transition into Final Projects.

### Module 4: Final Projects (Classes 16-20)

In teams, students create a full-stack web application that demonstrates command of all of the primary concepts discussed in this course. Overall, the application should make API calls, have dynamic functionality, and display a well-factored full-stack architecture. You act as a guide and support system for students as many project groups hit the occasional roadblocks and need assistance throughout the week. Otherwise, groups should be generally be self-managing. They will need to have proper Agile processes in place in order to keep their project in scope and delivered on time. See the project guidelines for more details. (TODO: Add the link to the project guidelines doc)

[-top-](#top)

---

<a id="materials"></a>
## Course Materials in this Repository

#### Lecture Guides

*Note that the Lecture Guides are not intended to be student-facing, but can be adapted as such.*

Within each of the adjacent class directories you'll find a README document containing the following:
- Overview of the day
- Daily learning objectives
- Daily readings
- Lecture topics
- Link to the lab README document

There is also a subdirectory within each daily directory that contains code demos that you may elect to use.

#### Lab Code

The feature tasks for each day's lab assignments are in the `labs/` directory of this repository. Each day is its own repository, so you will need to create a GitHub organization to host the lab repositories, create the individual repositories for each day, add the contents, and then publish them each day of class.

[-top-](#top)

---

<a id="operations"></a>
## Course Operations

Here's organizational tasks to keep in mind for each day as the class progresses:

- For the student-facing lecture repo, in each daily directory, a README should be generated that has, at a minimum, a daily class agenda, learning objectives, and links to readings and resources. That document can be an adapted version of the READMEs in the adjacent daily `lecture/` directories of this repository.
- The day's paired lab and individual code challenge should be prepped and poised for publication into the daily lab repository at the appropriate time in lecture. The code challenge should be released towards the end of lecture to prevent students from working on the lab assignment during lecture. The pair-programmed lab should be released at the start of lab time.
- It is strongly encouraged that the instructor open and test both the lab assignment and the lab solution each day; that is a solid reminder of the focus of the day, and preps you for seeing what the students will be seeing later.
- Don't forget to check for code demos in each adjacent daily directory!
- Be mindful of any items to be published in Canvas, and verify that the due dates on those items are correct prior to publication.

[-top-](#top)

---

<a id="organization"></a>
## Course GitHub Organization & Setup

##### Setting Up a New Class Repository

You should have a class repo (often referred to as the "course lecture repo") that lives in the Code Fellows account on GitHub. The name of the repository and subsequent informational fields should follow the patterns of the following example:

- **Name**: https://github.com/codefellows/seattle-301d18 (city, hyphen, course number, course specific code)
- **About**: "Class lecture repo for seattle-301d18. Lead Instructor: Sam Hamm"
- At the time of creating the lecture repo, a directory should be created for each day as seen in the example above.
- The README at the root level of your lecture repo should contain the same content as the example given above.

##### Setting up a Lab Organization and Individual Lab Repositories

- Each lab assignment should be a separate repository housed within a single organization, named in the pattern of this example: https://github.com/codefellows-seattle-301d18
- The individual lab directories can be copied over from the `labs/` girectory from this repository. Each daily lab will then need to be `git init`ed and have its remote set to a new corresponding repository within the lab organization.

[-top-](#top)

---

<a id="grading"></a>
## Course Grading & Prework; Other Academic Information

##### Grade Weightings

- The standard [course weightings](https://docs.google.com/document/d/1WnQkPbM1FzWxYgzhrayL_SerO80DXC4tybl-I1aiSUI/edit).

##### Prework

- Here is the prework GitHub repo link: [Code-301-prework](https://github.com/codefellows/code-301-prework)

- Prework assignments are graded like all others. This link should be shared with students by Admissions at the time of enrollment. It is wise to issue reminders to students to complete the prework in the days leading up to the start of the course.

##### Attendance

- Generally, students are expected to maintain a 90% attendance rate.
- Please refer to [Instructor Handbook](https://docs.google.com/document/d/1rByNEzSuJgUokU_kMXIxKzNotJSTIViwR1wdpP4HHDs/edit#bookmark=id.rydixnehkl2) for more information.

##### Quizzes

- Course quizzes are administered through Canvas. There is a total of six quizzes throughout the course, two per module. It is recommended that you review the quizzes so that you know exactly what the students will be seeing.

##### One On Ones

- Depending on class size, you may need perform a weekly, or at the least, a midway one-on-one pulse check on all students. This is also an ***extremely*** useful means of addressing the concerns of students that are revealed on the weekly surveys.

- A good way to start these conversations is to first ask "How’s it going?"

- If they reply with only a "good" or “okay” you can follow-up with “Anything in particular you want to talk about?” and keep things light before diving into any details below.

- The site youcanbookme.com is a handy way of scheduling one-on-one meetings. Aim for 15-minute time slots.

##### Whiteboarding (optional)

- This can be spread out across one or several days, usually time-boxed to 15-30 minutes (example spreadsheet for student sign-ups [here](https://docs.google.com/spreadsheets/d/119p29UJhGulpSpwJYRdTSAvtfXMvZom5VWiiq4VxVGg/edit?usp=sharing) with different slots being assigned to different instructors / TAs).

- A good starting guide for content can start with this problem domain:

- "We are tasked with modeling out buildings. We want to keep track of buildings in Seattle and are asked to pick up on just three initial properties that matter the most to us":

  1. The year that the building was constructed

  2. The number of floors that the building has

  3. The address the building is located

- With this information, help us build a constructor to model our buildings

Once they have a constructor, ask them to instantiate a new Building with the constructor, then have them write the output of what that new object would look like (including its properties and values).

- Next, propose a situation where the team has an **array** of these Building objects. For the sake of this example it can be an array of 3 buildings. We now want to target specific information about each building, and our job is to now retrieve **just the year** from each Building, and transform that into a **new array**.

- Guide the students to use Array.map() method to accomplish this goal, keeping in mind that in order to access this new array, they will need to save the result into a new variable.

##### Reading Assignments

- Reading is one of the primary language-learning processes that students will utilize to develop their skills. Each day, one or more reading assignment is due before the start of lecture. Students are expected to make at least one observation and ask a question to promote curiosity and class discussion. Their submission is completed by them and graded within your Canvas course. The reading submissions in Canvas are by default set up to be graded with either a ‘complete’ or ‘incomplete’ mark, and as a result, the late submission policy is not in effect for reading assignments.

##### Late Submission Policy

- [See Code Assignment Grading and Expectations](https://drive.google.com/open?id=0B9LDi5IfeIjCTHh6VU4yQV9ZaDQ)


[-top-](#top)

---

<a id="studentsetup"></a>
## Student Setup & Lab Workflow

The README for the first lab assignment (TODO: Add link) has detailed instructions for students in setting up their local directories on their laptops and also instructions in pair-programming process. Please refer there for more details.

[-top-](#top)
