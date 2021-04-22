Table of Content 
---

* [Eazyrecruit](#Eazyrecruit)
   * [Overview](#Overview)
   * [Setup](#Setup)
      * [Installation Guide](#Installation-Guide)
      * [Architecture](#Architecture)
   * [General Features](#General-Features)
   * [Screens in Depth](#Screens-In-Depth)
   * [Administration](#Administration)
   * [Commercial Support](#Commercial-Support)
   * [License](#License)

# EazyRecruit

An AI-enabled open source recruitment software to ease the screening and hiring process 

## Overview 
Eazyrecruit is a solution that is committed to the advancement of HR Talent Acquisition solutions. Its objective is to make the hiring process easy for employers and help them in acquiring the right talent from the market. It is an AI-enabled open source recruitment software to ease the screening and hiring process. It is an advanced and full-featured application for resume parsing, job listing, job sharing, applicant tracking, interview scheduling, interview ratings.

**What can EazyRecruit be used for?** If you have to fill in positions, even if it’s only one or two jobs a year, EasyRecruit can help you with ease. From SMEs to multinational companies, EazyRecruit can prove to be an effective hiring tool. From one user to hundreds.

EazyRecruit can work well for very high-volume recruiting. Importing and dealing with many candidates at once per role is allowed in EazyRecruit. It will handle all of recruiting, from job posting and applications, to initial candidate intake, scheduling the interview, offer, acceptance and candidate start. EazyRecruit was designed by recruiters, for recruiters and continues to be developed with recruiting as the sole focus.

## Setup

**Open Source Software**: EazyRecruit is open-source software. This means it is free to use, and you are free to modify it in any way you want. Seriously, if you want to do it, get down into the code and change absolutely anything!

**Web-based and local**: EazyRecruit can be installed in a variety of environments. For the solo recruiter/single user, EazyRecruit can be installed on your local computer, accessible only by you. It can also be installed and accessible via the internet, through a public-facing web server, so multiple users from all over the world can access and use the software together. _Make sure the appropriate measures are taken for the setup that you choose_. 

### Installation Guide

* Docker
   * sudo apt update
   * sudo apt install apt-transport-https ca-certificates curl software-properties-common
   * curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
   * sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu bionic stable"
   * sudo apt update
   * apt-cache policy docker-ce
   * sudo apt install docker-ce
* Source
   * Prerequisite
   * System Requirements : Ubuntu 18 (4 Core or Greater, 8 GB RAM or Greater)
   * Install Docker
   * Install Docker-Compose
   * Install Setup 
   * After repo cloning, copy example.env and create .env and update the variables listed there.
   * Run the command on root directory - `sh deploy.sh`
   * After successful setup, All the details such as web url, Admin Username and Admin Password will be displayed on the screen

* Languages Used
   * Python
   * HTML
   * JS, TS
 
* Framework Used
   * Angular
   * Expressjs
 
* Database
   * Mongo
   * Redis

### Architecture

![Architecture](https://i.ibb.co/XjSvp9F/Eazyrecruit-Architecture.png)

**Nginx**: A Nginx is an intermediary proxy service which takes a client request, passes it on to one or more servers, and subsequently delivers the server’s response back to the client.

**Engine**: It's a celery application, the main functionality of this module is to execute the tasks that are scheduled by the core service or periodically scheduled.

**Resume Parser**: It parses the name, email address, skills and other information from the resume uploaded by core service and after extracting the information it creates an applicant in the system for further process.

**Email Parser**: It checks the provided mailbox for new mails and analyzes them if it contains a resume or not, if it's a resume mail then this service downloads that resume and passes it on to the resume parser.

**Core Service**: It's an expressjs based application that provides endpoints for the client to access all services provided by Eazyrecruit.

* Job Portal
* Public APIs
* Web Admin

**Redis**: An open source, in-memory data structure is used as a celery broker for the system.

**MongoDB**: This cross-platform document-oriented database is used as a main db of the application to store all the information to make it more flexible.

**Elastic**: Elasticsearch is a highly scalable open-source full-text search and analytics engine. It provides the power of quick search to the system.

## General Features
Dig into the EazyRecruit capabilities and features to know more.

**Full recruiting life-cycle**: EazyRecruit provides the infrastructure for the entire recruiting life-cycle, regardless of the type of role that you are recruiting for, or the volume of openings that you are dealing with. It also works well for very high-volume recruiting. Importing and dealing with many candidates at once per role is easy in EazyRecruit. We can walk you through the process, including the sales cycle, from building targeted lead lists, making client calls, getting signed agreements and taking job orders. It will handle all of your recruiting tasks:

1. Job posting and applications
2. To initial candidate intake
3. Interview scheduling
4. Sending the offer letter
5. Acceptance and onboarding of the candidate

EazyRecruit is designed by recruiters, for recruiters and continues to be developed with recruiting as the sole focus. 

- **Jobs/Job Pipeline**
       In this section Admin/HR can create jobs with various details such as job title, Job description, Minimum/Maximum experience required for the Job, Meta image, Meta title, Meta description etc. 
       Admin/HR can make an option to publish the job so the job can be directly published on the company public job portal where all the job details will be reflected so that an applicant can see the job details and directly apply for the job.
       Admin/HR can add different pipelines with the name such as New, Pending, Hold, Select and Reject and add an applicant directly or can add from the applicant list which is already into the system. Added applicants will first insert into the first pipeline from where Admin/HR can move them into another pipeline according to interview results.
       - Create different jobs
       - Add applicant into a specific job
       - Track different job status

* **Interview Scheduler**
        In this section Admin/HR can select an applicant and schedule an interview to a specific interviewer.Admin can add various details such as job title, Interviewer name, Interview date/time and Interview round etc. during the interview schedule. Once an interview is successfully scheduled then Admin/HR, Interviewer and applicant will receive the mail with appropriate details.
 
* **Interviewer**
         We have implemented this section on user role base. An Admin/Hr can access all pending and completed interviews in this section and An interviewer can access all the pending interviews assigned to him where he/she can update the status of the interview, Rate to applicant skills and add comment over there.

     - **Analytics**
         Show number of resume received on the platform.With analytics the Admin can track how many 

     - **Social Sharing**
         The platform offers the possibility of sharing job requirement details added in the platform to be easily shared on various social platforms such as Linkedin, Twitter, Facebook. 

     - **Branding**
         The platform offers the facility of adding company details such as logo, name, as well as the option to include website address. The job listing page with the company’s branding adds an official touch to the experience. 

     - **Upload**
	       In this section Admin/HR can upload an applicant resume. The resume contains data such as applicant info such as name, email, experience, mobile number, skills, all 
         related information regarding applicants is parsed by the ML Text Recognition System, and related info is saved on our platform.

     - **Email Integration**
         We designed an automated system that parse every resume that is sent to the company email id, and the ML algorithms gather information about applicants.

     - **Public Job Portal**
         - Branding
            Company details such as company logo, name, website can easily be customised.
         - Publish Job Listing
            All the publishing jobs will be listed here.
         -  Job Apply
            Candidates can apply for a specific job.
         - Social Sharing
           Share jobs on various social platforms such as Linkedin, Twitter, Facebook.

**Support**: We have an active community of people that are willing to help as much as possible though. Also, we are slowly adding to our documentation. 

**Intuitive interface**: EazyRecruit has an easy to use, intuitive interface. This means minimal training time for you. The job portal also has a simple search and application process that your candidates will get through easily.

**Skills-based tagging**: Skill-based tagging serves as a very functional alternative to keyword searching. Within EazyRecruit, one can make a list of skill-sets required for the job. The candidates matching that criteria can be narrowed down easily.

**Calendar**: EazyRecruit has a rich calendar built-in that provides a thorough and accurate overview of interview schedules. If you use the calendar system, you will always know what is coming up, and be able to quickly find information from past scheduled events. The calendar can be synced with Google for calendar import and access.

**Ownership of data**: You own the data control and its security. No need for your data to be on someone else’s servers, unless that is how you choose to do it. 

**Backup and restore**: Your EazyRecruit system can be backed up as often as you want, ensuring no loss of data, ever.

**User access levels**: There can be different access levels for users in the EazyRecruit system, which the administrator can set up and assign.

**Built-in Emailing**: The email functionality within EazyRecruit is substantial. Currently, EazyRecruit can be used to send emails to candidates, clients, and contacts. It can also be used to notify of status changes and new applications, or anything you would like it to do.

## Screens in Depth 
   
   The EazyRecruit platform is made up of the following modules: 

**Login**: One can log in at EazyRecruit via Gmail or work email. The admin account has the major controls of the platform and the admin can only allow access to other people. 

**Home**: As an admin or a user when you log into EazyRecruit platform, you will see the Home section. This is your dashboard, which shows the monthly calendar and informs you about the interviews scheduled for the day. On the Home screen, one can also see the number of users who are visiting the platform as well as the resumes received segregated through channels. 

**Jobs**: In this section, all the Job listings are displayed. When one clicks on the “Active Jobs” tab, they will be able to see the current openings in the company. The “Archive Jobs” tab displays all the jobs created on the platform to date. The jobs which have been fulfilled or the ones that you are no longer interested in hiring. By clicking on the “+Create” tab one can create a new job listing for the company. One can mention the:
   * Job Title
   * Job Type
   * Annual Salary
   * Minimum/Maximum Experience
   * Job Location
   * Expiry Date (The day when you wish the job listing to be removed)
   * Skills
   * Job Description
   * Job Responsibilities
      
**Note**: The “Active tab” on the right-hand corner of the create job page denotes that one wishes to hire for the open position within the company or via current employee references. The Publish tab, however, means that the job opening is open for all potential appliers.

**Applicants**: All of the applicants that have applied for various job profiles in your company are available here. One can search applicants via:
* Date- A particular time duration in which the candidate must have applied for the job
* Source- The candidate applied for the job via email, website, or on the platform, or their resume was uploaded by the admin.
* Job – One can also search for a candidate/s via Job Title
* Search Bar – In the search bar on can type the name of the candidate, job profile, or skill set.
* The master sheet shows the:
   * Candidate’s Name, Email and Phone Number
   * Experience  	
   * Salary 
   * Notice Period 
   * Source
   * Job
   * Status - New/Awaiting Response/ER Interview/Selected/Rejected

**Interview**:
* Status - Stage of the interview, scheduled by, date, and time
* Schedule - Date, Channel as well as the Meeting link for the interview (in case of an online interview)

**Profile**: In the profile section one can update: 
* First Name 
* Last Name 
* Email Address
* Contact Number 
* Profile Photo

**Note**: The Login password for the profile can also be changed by entering the old password. 

**Database**: The database contains all the list of the candidates: The candidate's information is listed under the following headers:
* Candidate
* Experience
* Salary	
* Notice Period	
* Source	
* Skills
                   
A candidate can be added to the database by clicking on the "Create" tab. One can add information like: 
* First Name, Middle Name, Last Name
* Email Address
* Contact Number 
* Referred by 
* Availability 
* Notice Period
* Experience 
* Skills
* Current and Expected CTA
* Current Location
* Resume
                       
If the admin wishes to upload multiple resumes they can do so by clicking the ‘Upload’ button and enter information in the database.

**Settings**: Options to customize your account and features are available in this module. Users change their Profile, Password. Administrators access your account, change your Career Portal and Email configurations, and customize your dashboard, import and backup data.

**Details Tab**: Under the ‘details’ tab one can customize the job opening page according to the company’s branding. 
* Company Logo
* FavIcon
* Company Name
* Company Website
* Address 
* Company Email Address
* Company Phone No.
* Company Header Description
* Company Header Color
* Company Header Text Color

**Users Tab**: Under the Users tab one can all the members who were given access to the Eazyrecruit platform by the admin. The admin can see the role assigned to each member and the admin can also edit or delete the rights. 

If the admin wishes to add a new member on the platform, they can do so by clicking on the “+ Create” button and add information about them in the below-mentioned manner: 
* First Name
* Last name
* Email Address
* Contact No.
* User Role


**Skills**: Here the admin can add ‘n’ number of skills that they are looking for in a candidate.  

When the need arises to add a new skill, the admin can do it by clicking on the “+Create” icon and just adding the skill name in the box as shown below. 

**Applicants** - Under the ‘Applicants’ tab, the admin can choose to ‘Reprocess resumes’ or ‘Resync Database’ in order to keep the information updated. 

**Email Settings** - We offer the option to select between work email, Gmail account or third-party email via SMTP. One can design and configure email here, the preview of which is shown like the image below. The email template customization can be done using the ‘Edit’ link at the bottom of the page. By use of simple HTML and CSS, the email header, body, as well as footer can be defined. 

**Google Analytics** - The company webpage, where the fresh job requirements are in general posted can be tracked via Google Analytics on the EazyRecruit platform.

**Google Recaptcha** - In order to confirm that the job postings are being filled by candidates only and not bots or spam, Recaptcha can be added at the end of the job details.

## Administration

**Email Settings**
* Inbound Settings (imap)
Configure Imap to fetch resume from specific email-id.

* Outbound Settings
Configure smtp to send emails.

* Email template Preview
Preview and configure the email template that is sent to the applicant.

**Branding**
In this section of the platform, the admin can customize the job hiring page according to the company’s branding. The admin is free to add company details including:
company name;
* logo of the company;
* company favicon;
* company address;
* contact number;
* company header description;
* header color etc.

![Admin](https://i.ibb.co/DG6c6FZ/Eazyrecruit-Admin.png)

**Backup and Restore**
Each and every critical business software must have a backup and restore process in place to keep disasters at bay. There are a few methods with which you can backup and restore the EazyRecruit system. When setting up a backup and restore system at EazyRecruit, what one needs to keep in mind is the fact that - 
* How often should you initiate backup? 
* How often should one test their backup? 
* Where will your backup be stored? 
* Is there a need to automate the backup process?

**Google Login**
A user can login by Google Account into the Admin panel. First that user should be registered into the admin panel then only he/she can login into the admin panel. 

**Analytics** 
The admin panel offers detailed information related to the number of people visiting the website along with how many candidates are applying for the jobs. The information is added in a date-month pattern. Moreover, with analytics the admin can also track segregated information about the route a candidate took to apply for the job - email, webpage, or the resume was directly shared on the job listing. Out of all the resumes reaching the system how many of them were uploaded in the database can also be tracked from here.

## Commercial Support 
We offer commercial support via our enterprise product EazyRecruit. Please visit https://www.eazyrecruit.in/ for more details.

## License
Copyright (c) [2021] [Eazyrecruit]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
