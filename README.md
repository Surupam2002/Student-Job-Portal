# Student Job Portal (Java EE · JSP · Servlets · MySQL)

A full-featured job portal web application for students and freshers, built with **Java Servlets, JSP and MySQL**. Candidates can create a profile, build or upload a resume, search jobs by technology or location, and apply. All applications are tracked in one place.

## Features

**Accounts & security**
- Registration and login with cookie-based "remember me" sessions
- Logout and session handling
- Server-side input validation with a servlet **Filter**

**Candidate profile**
- Edit "About" section and upload a profile picture
- Add, edit and delete **education** and **work experience** entries
- Upload and download a resume
- **Resume builder**: generate a downloadable resume from profile details

**Jobs**
- Search jobs **by technology** and **by location**
- Browse companies and their open jobs
- View job descriptions and **apply in one click**
- **My applied jobs** page, with the option to withdraw an application

**Other**
- Contact-us form, About page, custom error pages

## Tech Stack

| Layer | Technology |
|---|---|
| Backend | Java, Servlets, JDBC |
| Frontend | JSP, HTML, CSS |
| Database | MySQL |
| Libraries | MySQL Connector/J, Apache Commons IO (file uploads), PDF library (resume builder) |
| Build / IDE | Apache Ant, NetBeans |

## Project Structure

```
Student-Job-Portal/
├── jobportal.sql                 # Database schema and seed data
├── JAR/                          # Required libraries (MySQL connector, Commons IO, PDF)
└── web_JobPortal_19/
    ├── build.xml                 # Ant build file
    ├── src/java/com/mahid/
    │   ├── backend/              # Servlets: Login, Register, ApplyForJob, ResumeBuilder,
    │   │                         #   JobSearchByLocation, JobSearchByTechnology, ...
    │   └── connection/           # DbConnection.java + db.properties
    └── web/                      # JSP pages, CSS, images, WEB-INF
```

## Getting Started

1. **Database:** create the database and import the schema:
   ```bash
   mysql -u root -p < jobportal.sql
   ```
2. **Configure the connection:** edit `web_JobPortal_19/src/java/com/mahid/connection/db.properties` with your own MySQL URL, username and password.
3. **Open the project** `web_JobPortal_19` in **NetBeans** and add the JARs from the `JAR/` folder to the project libraries.
4. **Run** on a Java EE servlet container such as **Apache Tomcat**, then open the app in your browser.

## Author

**Surupam Kumar Pandey** · [GitHub](https://github.com/Surupam2002) · [LinkedIn](https://www.linkedin.com/in/surupam-kumar-pandey-44b293218)
