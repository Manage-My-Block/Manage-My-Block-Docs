# Quentin McKay & Matt Garrow - T3A2-A - Full Stack App (Part A)

## Authors

Quentin McKay - [GitHub](https://github.com/quentin-mckay) | [Portfolio](https://www.quentinmckay.dev/) | [LinkedIn](https://www.linkedin.com/in/quentinmckaydev/)

Matt Garrow - [GitHub](https://github.com/mjkgarrow) | [Portfolio](https://matt-garrow.netlify.app/) | [LinkedIn](https://www.linkedin.com/in/matt-garrow/)

## Project links

- [Github repo](https://github.com/Manage-My-Block/StrataSphere-Docs)
- [Project presentation]()
- [Trello board](https://trello.com/b/L4fMRj3x/term-3-full-stack-project)


## Index

- [Description](#description)
- [Purpose](#purpose)
- [Functionality/Features](#functionality--features)
- [Target Audience](#target-audience)
- [Tech Stack](#tech-stack)
- [Dataflow Diagram](#dataflow-diagram)
- [Application Architecture](#architecture-diagram)
- [User Stories](#user-stories)
- [Wireframes](#wireframes)
- [Planning methodology](#trello-board)

## R1 - APP DESCRIPTION
### Description

StrataSphere is a building management tool that allows Owners Corporation Managers, Owners Committee Members, and Building Members to stay on top of everything happening in their building - from official capital works to who is throwing the next BBQ or block party.

### Purpose

The current problem is that many buildings are managed in an informal way, with committee members messaging and emailing individually with little transparency, while the owners corporation management are unable to collate all the information about the building, as well as lacking their own communication and responsibility transparency. While there exists some forms of management software (such as Trello), these are unequiped for managing a building that needs to conform to state building management codes as well as maintaining building security. This app aims to tackle these issues.

### Functionality & Features

#### Features:
- Public notice board with comments
- Ticket board (similar to todo items), with comments
- Voting mechanism within Tickets
- Meeting scheduler
- Budget tracker
- Authentication and authorisation

#### Functionality
- Admin roles can CRUD users/tickets/posts/votes/meetings/contacts/budget
- Committee member roles can CRUD tickets/posts/comments
- Building member roles can CRUD their own posts/comments

### Target Audience

This is an enterprise-facing application. The application will be provided for internal use by a Owners Corporation Management company that can then allow access to building members. The target audience will be the owners corp management and the owners/occupants of a building. Future updates could allow multiple buildings to be managed through the one account, but for the first version each instance of the app will only manage a single building.

### Tech Stack

This is a MERN application:
- MongoDB: A document-oriented database for storing data.
- ExpressJS: The server framework that manages requests/responses, including the business logic in the back-end of the application.
- React: The front-end framework for building the client-facing views. We have used Vite to build the React scaffolding.
- Node: The JavaScript runtime environment that creates the server that ExpressJS runs on.

Deployment:
- Render: Node/Express server deployment through Render.com
- MongoAtlas: Database stored on MongoDB cloud service, Atlas
- Netlify: React front-end deployed on Netlify

---

## R2 - DATAFLOW DIAGRAM <a id="dataflow-diagram"></a>
[Provides dataflow diagram(s) that strictly follow the standard convensions to clearly identify the processes within your application. Clearly depicts where data is coming from, where it is going and how it is being stored.]

Dataflow Diagram:
<p align="center">
  <img src="./docs/dataflow_diagram.png" />
</p>

---

## R3 - APPLICATION ARCHITECTURE DIAGRAM <a id="architecture-diagram"></a>
[Shows almost flawless understanding of the high level structure of the app]

Application Architecture Diagram
-- TODO --

---

## R4 - USER STORIES <a id="user-stories"></a>
[Provides multiple user stories that use ‘persona, what and why’ that outline meaningful features of project. Shows evidence of user story revision and refinement.]

The app will have 3 types of user:
- #### **Owners Corporation Manager**
    This is an 'admin' role, they can CRUD users/tickets/notice board posts/meetings. They can also create data in the app such as adding contact information for services (plumber, elevator, electricians, etc), adding apartment numbers (to assign to users), approving the Owners Committee members, updating the budget balance. They can call votes, approve votes, and add minutes to meetings.

    Owners Corporation Managers are people who are part of a company that manages buildings to comply with state and national housing laws. Most buildings have Owners Corporation Managers, however it is possible for smaller units to self-manage. Both kinds of manager can use the StrataSphere app.

- #### **Owners Committee Members**
  Owners Committee Members have all the abilities of a standard *Building Member* but can also cast votes when the Owners Corporation Manager calls a vote and CRUD tickets/notice board posts.

  Committee members are a voluntary position in a owners corporation. They are owners of apartments in the building and they can request to join the committee after each Annual General Meeting, which is where Owners Corporation Managers present budget outcomes and owners can voice concerns. It is often the case that each year the committee members will change.

- #### **Building Member**
  This is the standard role in the app. They can CRUD their own notice board posts and comment on posts. They can only read information about committee members, the owners corporation manager, other building members, services contact info, and tickets. They cannot create tickets, that needs to be done by a Owners Committee Member. All Building Member abilities are shared with Owners Committee Members.

  Building members can be owners or occupants of apartments in the building. While similar building management apps restrict users to owners only, StrataSphere allows for a more open environment where renters and other occupants can participate in the building management. However, because this type of user may not be legally entitled to make decisions StrataSphere restricts the role to only the notice board and viewing data for contacts and other users.


#### Owners Corporation Manager User Stories
- "As an Owners Corporation Manager, I want to only allow approved building occupants to access the application, so that we can maintain building security."

- "As an Owners Corporation Manager, I want to be able to CRUD users, so I can make sure the users are approved occupants of the building with the correct contact information."

- "As an Owners Corporation Manager, I want to be able to schedule a meeting with the Owners Committee, so that we can discuss tickets and provide feedback"

- "As an Owners Corporation Manager, I want the ability to call a vote on tickets and approve the vote, so that there is input from the Owners Committee members that is officially recorded."

- "As an Owners Corporation Manager, I want to be able comment on tickets, so that I can provide additional information for committee members and show how the work is progressing."

- "As an Owners Corporation Manager, I want the finalise and close tickets, so that I can show the progress being made and keep the tickets log organised."

- "As an Owners Corporation Manager, I want to be able to moderate the notice board, so that I can keep it organised and remove unwanted posts."

- "As an Owners Corporation Manager, I want to be able to add contact information, so that building occupants can easily access emergency contacts to manage tickets."

- "As an Owners Corporation Manager, I want to be able to approve Owners Committee members, so I can update the roster after each Annual General Meeting."

- "As an Owners Corporation Manager, I want to be able to update the budget, so that I can inform the occupants how much money we have remaining in the budget."

#### Owners Committee Member User Stories

- "As an Owners Committee Member, I want to be able to CRUD tickets for issues in the building, so that I can inform the owners corporation management of repairs/problems."

- "As an Owners Committee Member, I want to be able comment on tickets, so that I can provide additional information for other committee members and owners corp management."

- "As an Owners Committee Member, I want to be able to CRUD posts on the notice board, so that I can have discussions with other building members about topical issues in the building."

- "As an Owners Committee Member, I want to be able to cast votes on tickets, so that I can perform my task as a committee member and approve of any works that need to be done."

#### Building Member User Stories

- "As a building member, I want to be able to see information about committee members, managers, and other building members, so that I have access to contact information and a clear understanding of who is involved in my community."

- "As a building member, I want to be able to see the contact information for building services, so that I know who to contact when necessary."

- "As a building member, I want to be able to be able to create, update, and delete my posts on the notice board, so that I can contribute to notice board posts."

- "As a building member, I want to be able to see basic budget information, so that I understand the current state of the budget to provide context for the meetings."

### User Story first refinement

We added some additional admin abilities to the Committee persona as we felt like they should have similar abilities. The only thing that a committee member can't do is CRUD other users

#### Owners Committee Member User Stories

| **I want to...**              | **So I can...**                                                                                       | **Related Feature**                                       |
| ----------------------------- | ----------------------------------------------------------------------------------------------------- | --------------------------------------------------------- |
| CRUD a ticket                 | inform the owners corporation management of repairs/problems                                          | Create a Ticket if committee member                       |
| Comment on Tickets            | provide additional information for other committee members and owners corp management                 | Ticket commenting if committee member                     |
| Vote on a Ticket              | perform my duty as a committee member and approve of any works                                        | Cast a vote on a Ticket if committee member               |
| CRUD the Notice board         | keep the notices organised and remove unwanted posts, as well as talk about goings-on in the building | CRUD any notices/comments if committee member             |
| Change the status of a Ticket | Start or close a ticket if the work is complete                                                       | Set status and set complete on Ticket if committee member |
| Add a cost to a ticket        | To show how much something cost                                                                       | Set Ticket cost and update Budget if committee member     |
| CRUD a Meeting                | provide feedback to the committee and call an AGM                                                     | CRUD Meetings if committee member                         |
| Call a vote on a Ticket       | Confirm the committee members approve the action required                                             | Call a vote on Ticket if committee member                 |


### User Story final refinement

We have taken the user stories and combined them with specific features. We have also streamlined some of the stories so we have a clearer understanding of how features and UX will interact.

#### Owners Corporation Manager User Stories

| **I want to...**              | **So I can...**                                           | **Related Feature**                            |
| ----------------------------- | --------------------------------------------------------- | ---------------------------------------------- |
| Call a vote on a Ticket       | Confirm the committee members approve the action required | Call a vote on Ticket if admin                 |
| Comment on Tickets            | Provide feedback on the work taken                        | Ticket commenting                              |
| Change the status of a Ticket | Start or close a ticket if the work is complete           | Set status and set complete on Ticket if admin |
| Add a cost to a ticket        | To show how much something cost                           | Set Ticket cost and update Budget if admin     |
| Approve committee memebers    | update the roster after each Annual General Meeting       | CRUD users if admin                            |
| CRUD the Notice board         | keep the notices organised and remove unwanted posts      | CRUD any notices/comments if admin             |
| CRUD a Meeting                | provide feedback to the committee and call an AGM         | CRUD Meetings if admin                         |

#### Owners Committee Member User Stories

| **I want to...**              | **So I can...**                                                                                       | **Related Feature**                                       |
| ----------------------------- | ----------------------------------------------------------------------------------------------------- | --------------------------------------------------------- |
| CRUD a ticket                 | inform the owners corporation management of repairs/problems                                          | Create a Ticket if committee member                       |
| Comment on Tickets            | provide additional information for other committee members and owners corp management                 | Ticket commenting if committee member                     |
| Vote on a Ticket              | perform my duty as a committee member and approve of any works                                        | Cast a vote on a Ticket if committee member               |
| CRUD the Notice board         | keep the notices organised and remove unwanted posts, as well as talk about goings-on in the building | CRUD any notices/comments if committee member             |
| Change the status of a Ticket | Start or close a ticket if the work is complete                                                       | Set status and set complete on Ticket if committee member |
| Add a cost to a ticket        | To show how much something cost                                                                       | Set Ticket cost and update Budget if committee member     |
| CRUD a Meeting                | provide feedback to the committee and call an AGM                                                     | CRUD Meetings if committee member                         |
| Call a vote on a Ticket       | Confirm the committee members approve the action required                                             | Call a vote on Ticket if committee member                 |

#### Building Member User Stories

| **I want to...**                      | **So I can...**                                          | **Related Feature**             |
| ------------------------------------- | -------------------------------------------------------- | ------------------------------- |
| CRUD the Notice board                 | talk about goings-on in the building                     | CRUD their own notices/comments |
| View contact and building member data | know who to contact in an emergency or to discuss issues | View all contacts and users     |
| View budget data                      | understand how my body corp fees are being spent         | View budget and transactions    |


---

## R5 - WIREFRAMES <a id="wireframes"></a>
[Provides wireframes that show exceptional planning of project flow and structure including but not limited to space distribution, content prioritisation, intended actions, functions, relationships between screens.]

Wireframes for multiple standard screen sizes, created using industry standard software
-- TODO --

---

## R6 - PLANNING METHODOLOGY <a id="trello-board"></a>
[Simple and clear standards for planning methodology chosen and adhered to]  

Tasks are organised using [Trello](https://trello.com/b/L4fMRj3x/term-3-full-stack-project).

For our planning methodology we went with a simplified version of Kanban, while adhering to Agile procedures such as sprints, reviews and definition-of-done. At the start of each sprint we create the tasks, which are broken down into 'cards' and placed in the 'Current Sprint' bin. We then assign the tasks to each team member. Tasks move from left to right as they are completed. We also used a 'blocked' bin, which helps signal when a person is waiting on another piece of work to complete their task.

We used a colour-code system to visually see how long each task is estimated to take. We have estimates from 1 hour to 1 week. We try to limit the cards to a max of 2 days though some cards, like the wireframes, were estimated to take over a week. At the end of each sprint we review the estimates and update expectations based on improved effeciency.

<p align="center">
  <img src="./docs/trello_screenshots/colour-coding.png" />
</p>


Rubric items were also added to the Trello so we can track how the assignment is progressing and to have 'definition of done' for our sprints/cards.

<p align="center">
  <img src="./docs/trello_screenshots/rubric-items.png" />
</p>


### July 5:

### July 6:
<p align="center">
  <img src="./docs/trello_screenshots/July%206_1.png" />
</p>

<p align="center">
  <img src="./docs/trello_screenshots/July%206_2.png" />
</p>

<p align="center">
  <img src="./docs/trello_screenshots/July%206_3.png" />
</p>

### July 7

Matt split his tasks into more manageable cards to maintain a 2-4 hour window for tasks. This kept him more focused and on track, plus it had the added benefit of visualising the burn-down.

<p align="center">
  <img src="./docs/trello_screenshots/July%207_1.png" />
</p>

### July 9

Quentin started work researching the front-end technologies. Quentin also took on the Wireframe work, while Matt took the Dataflow Diagram work.

<p align="center">
  <img src="./docs/trello_screenshots/July%209_1.png" />
</p>

### July 10

Slowly burning down the work. Quentin completed a few of his research tasks.

<p align="center">
  <img src="./docs/trello_screenshots/July%2010_1.png" />
</p>

### July 11

Matt did a review and re-work of the dataflow diagram to incorporated some feedback provided.

<p align="center">
  <img src="./docs/trello_screenshots/July%2011_1.png" />
</p>

Matt completes his tasks and begins finalising the README document for submission. Quentin still working on Wireframes. Those tasks require a review into thier estimated work time.

<p align="center">
  <img src="./docs/trello_screenshots/July%2011_2.png" />
</p>

### July 12

Matt does a review of the User Stories. There was discussion about the level of authorisation given to Committee Member users - the outcome being that they should have the same abilities as an admin but without User CRUD.

<p align="center">
  <img src="./docs/trello_screenshots/July 12_1.png" />
</p>

Wrapping up the last bits of the project. Matt takes on the task of ensuring the readme document is complete and correct.

<p align="center">
  <img src="./docs/trello_screenshots/July 12_2.png" />
</p>

A new item is added to the current sprint - video presentation work.

<p align="center">
  <img src="./docs/trello_screenshots/July 12_3.png" />
</p>

The final piece of the project: getting it ready for submission.

<p align="center">
  <img src="./docs/trello_screenshots/July 12_4.png" />
</p>