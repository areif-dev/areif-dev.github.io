---
layout: default
title: "Artifact 3: Fullstack with PostgreSQL"
---

{% include nav.md page="/fullstack-with-postgresql" %}

## Artifact 3: Fullstack with PostgreSQL

## Competency: Databases

### Repo Links

- Original Code: <a href="https://github.com/areif-dev/cs465-fullstack" target="_blank">https://github.com/areif-dev/cs465-fullstack</a>
- Enhanced Code: <a href="https://github.com/areif-dev/cs465-fullstack/tree/enhancements" target="_blank">https://github.com/areif-dev/cs465-fullstack/tree/enhancements</a>

### Description

This artifact is from CS 465. I completed the original version in my senior year. It’s purpose was to demonstrate my ability to develop a fullstack web application complete with a database, a user facing website, and an administrative web app. The application was built using the MEAN stack, which stands for MongoDB, Express, Angular, and Node, so the project was written in JavaScript and used MongoDB for the database.

|                 Travlr Class Diagram                 |
| :--------------------------------------------------: |
| ![travlr_class_diagram](/assets/imgs/travlr_uml.png) |

### Justification

This project showcases my knowledge of numerous technologies such as MongoDB, PostgreSQL, Node.js, Express, and Angular. It is also a great example of my ability to develop a full stack web application completely from scratch. The project also shows that I'm capable of migrating a project to a completely different database if necessary.

Most of the enhancements I made to this project are in the app_api folder. This is the directory that handles interactions between the database and a REST API built with Express. More specifically, the db.js file in the database directory handles connecting to a Postgres instance and sharing that connection with the rest of the code. That connection is then used by the Trip and User models defined in the database/models directory to handle CRUD operations.

### Objectives

My primary objective with this artifact was to demonstrate an ability to use well-founded tools in computing practices for the purpose of implementing computer solutions that deliver value and accomplish industry-specific goals. I accomplished this objective by modifying a full stack web application to use PostgreSQL instead of MongoDB.

I also achieved the goal of developing a security mindset that anticipates adversarial exploits in software architecture and designs to ensure privacy and enhanced security of data and resources by writing the database connection to require a non-root level user for managing the Travlr database and storing the password the that user in a file outside of version control.

### Reflection

Although I have used relational databases in the past, I have never used PostgreSQL, so the first thing that I learned while enhancing this project was how to work with Postgres. I learned how to install it with Docker and manage users, databases, and tables with the psql utility. Once I had the database setup, I also learned how to access the database from Node using node-postgres or "pg" as the package is called. This library handles connecting to a Postgres database as well as sending queries.

One challenge I faced while working on this enhancement was the unspecific error messages that node-postgres returns when it encounters a problem. A few times I experienced problems while trying to insert records because the insert query did not line up with the table's schema, but node-postgres would not tell me exactly which column was the problem.
