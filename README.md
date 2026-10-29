# University Application Tracker

Students applying to universities have to manage many deadlines,
documents, and requirements at once, and it's easy to miss something.
This command-line-style tool helps students (and the people who help
them) see which applications are in progress, which documents are
still missing, and which deadlines are coming up next.

**Users:** high school students applying to university, and advisors
or tutors who support them.

**Interface track:** Track A (tkinter), written by me without AI.

## Modules

| Module | Purpose |
|---|---|
| Universities | Keeps the universities students can apply to |
| Applications | Keeps each student's applications and their status |
| Documents | Keeps the documents each application requires |

## Functionalities

**Universities**
1. Add a university: name, country, deadline, fee -> new university record
2. Update a university's deadline or fee: university ID, new deadline or fee -> updated record
3. Remove a university: university ID -> confirmation message
4. List universities by country: country -> matching universities sorted by deadline

**Applications**
5. Start an application: student name, university ID -> new application with status "Not started"
6. Update application status: application ID, new status -> updated application
7. Search applications by student: student name -> that student's applications
8. List upcoming deadlines: number of days -> applications due within that time, soonest first

**Documents**
9. Add a required document: application ID, document name -> new document record
10. Mark a document as submitted: document ID -> updated document record
11. List missing documents: student name -> documents not yet submitted
12. Show application progress: application ID -> percentage of documents submitted

## Data each module keeps

| Module | Fields |
|---|---|
| Universities | university_id, name, country, deadline, fee |
| Applications | application_id, student_name, university_id, status |
| Documents | document_id, application_id, name, submitted |

Sample data (10 records each) is in the `data` folder:
`universities.csv`, `applications.csv`, `documents.csv`.
All student names are made up.
