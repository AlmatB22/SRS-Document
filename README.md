# Software Requirements

# Specification

## for

# Volunteer Management

# System (VMS)

### Version 3.0 approved

### Prepared by Emiliano Garcia (T00667348)

### Almat Bolatbekov (T00667348)

### 2022-11-

**_Copyright © 1999 by Karl E. Wiegers. Permission is granted to use, modify, and distribute this document._**


## Table of Contents

- 1. Introduction
   - 1.1 Purpose
   - 1.2 Intended Audience and Reading Suggestions
   - 1.3 Product Scope
- 2. Overall Description
   - 2.1 Product Perspective
   - 2.2 User class and Characteristics
   - 2.3 Operating environment
   - ○ 2.4 Design and Implementation Constraints
   - ○ 2.5 Assumptions and Dependencies
- 3. Data Requirements
   - 3.1 User Interfaces
   - 3.1.1 User Profile
   - 3.1.2 Service Requests Page
   - 3.1.3 Volunteer approval page
- 4. System Features
   - 4.1 Create new volunteer
   - 4.2 Assign volunteer
   - 4.3 Generate Daily Report
- 5. Other Nonfunctional Requirements
   - 5.1 Performance Requirements
   - 5.2 Safety Requirements
   - 5.3 Security Requirements
   - 5.4 Software Quality Attributes
- 6. Other Requirements
- Appendix A: Glossary
- Appendix B: Analysis Models


## Revision History

**Name Date Reason For Changes Version**


## 1. Introduction

### 1.1 Purpose

```
After a drop in volunteer participation after the COVID-19 pandemic it has become abundantly
clear that a volunteer management system is needed. At this time manual volunteer assignment
takes two weeks which is unacceptable if the volunteer numbers are to return to a healthy number.
The majority of the assignment time is spent manually performing background checks that take on
average 10 days. However, with the automated checking system that will be ready in time for
system deployment this time would be reduced to only 48 hours. In addition to helping seniors with
daily tasks, a new system would allow volunteers to support students with tutoring and coaching in
extracurricular activities.
```
### 1.2 Intended Audience and Reading Suggestions

**Stakeholder Major Value Attitudes Major Interests Constraints**

Government higher
organization

```
see the system as
means to decrease
work and
operational costs
```
```
efficient, quick, proact
and time-saving system
with automated
processes and alerts
```
```
compatible with
police and
school systems
```
Volunteers simpler
process

```
appreciate high
usability and
intuitive design
```
```
ease of use and
accessible
```
```
must run on
many different
devices
```
Elementary
education

```
access to
extra services
```
```
expect easy to use
and compatible
interface
```
```
ability to interact with
school systems; the low
learning curve for staff
```
```
no budget for
modifying
current system
```
Downtown
business

```
increased
revenue
```
```
customizable and
tailored for the local
business
```
```
simple to add
promotions without
disrupting business
```
```
Can’t take too
much time to
use
```
### 1.3 Product Scope

```
The main function of the Volunteer Management system is to add the number of volunteers and
connect them with senior people. The product is intended to give benefits to the senior people by
saving time, this is achieved by reducing the waiting period so that they will get the volunteer
services within three days. The system processes the registered volunteers' data in the system and
sends this information to the police certificate check system automatically, which results in a
```

shrinking time for the overall volunteer assignment process. The data processing and sending
information to the police certificate check is also a benefit for the volunteers, the reason is that our
system gathers volunteers’ data so that there is no need for them to go and apply for the certificate
manually. This feature will save a lot of time for the volunteers and attract them to these activities.

## 2. Overall Description

### 2.1 Product Perspective

Assigning a senior person and the volunteer requires management of the data and end-user services
to access the data. The data will be coming from the senior people and volunteers' inputs of their
personal information such as interests, preferences, and location. The software system described in
this SRS can enable the automation of the required tasks such as processing volunteer accounts and
assigning volunteers to senior cases.
The SRS describes the software that depends on a Background system check. The information from
the VMS is sent to the police BCS to check the history of the volunteer when they apply for the
volunteer account.

### 2.2 User class and Characteristics

The users of the Volunteer Management system will include volunteers, senior people, software
developers, SPCC employees, and others (in the giventable below you can see the user classes for the
Volunteer Management system). All users should befamiliar with web technology, however, the
majority of the senior people will not be able to use the system, which is why SPCC employees will
help them.

In the given table below you can see the user classes for the Volunteer Management system.

```
User class Type Description
```
```
Certified
Volunteers/
Senior-peer
```
```
Direct/
Favoured
```
```
Senior people report their need for social support once they will require
this service. They are one of the main users of this system and elderly
people will use the system quite often to find themselves a senior peer for
their basic needs. The senior person will have to give information by
phone to the SPCC employee to register. They need to see the list of the
volunteers that are appropriate depending on the given information by the
senior person.
```

Senior people Direct /
Favoured

```
Volunteers will see the list of the senior people who are in demand of
social support services. They put their information such as personal data,
hobbies, and others in the VMS and have to be approved by the police
certificate check. Volunteers’ services will include making daily calls to
the senior people and reminding important dates (such as medical
appointments). Moreover senior peer will be responsible for following up
on the social status and mental status of the elderly person, to report any
health issues to the VMS. Volunteers will not be able to see the student’s
or senior’s information unless he or she is matched with them. They will
use the VMS more than the senior people, to see any updates of their
volunteer activities.
```
SPCC
Employee

```
Direct SPCC employees receive calls from senior people to collect their
information over the phone, and create profiles for senior people at the
VMS. They are also able to change this data later in the profiles if any
updates occur. Each SPCC employee will use the system the same as the
senior person as all the process is going through them. They need to call a
volunteer senior peer when the senior person reported about the needed
support.
```
Volunteer
Administrator

```
Direct Volunteer administrators process the data of the newly registered
volunteers and make decision about their
```
```
application, if the profile looks ok their profiles go to the police
background check.
```
```
They also should verify the educational certificates of the volunteers
who need to teach young kids. Volunteer administrator will receive the
forecast number of cases for the next week by the VMS and receive any
report about any issues of the volunteers’ commitment activities to take
proper actions. The are going to use the system often but not the main
features of the VMS.
```
Police officers Indirect Police officers will receive the volunteer information and check its
background after the volunteer management approves the application.
They will do it only during the working hours as the BCS is required
the manual step to get approval

Students/Kids Indirect The Kids will receive the volunteer teaching services but they will be
allowed to use the actual system as the parents do not like to let the kids
use this type of applications


```
Uncertified
Volunteers
```
```
Disfavoured The volunteers who could not pass the background check system or the
application was not good enough for the volunteer administrator
```
```
School principleDirect The School administration will request volunteers to teach students.
Since the students will not be able to use the system, the school
principle would create an account and request for the services.
```
### 2.3 Operating environment

The server-side components should be operated within an operating system environment.
The client-side components of the software system must operate within web browser
environments, The minimum browsers that must be supported are:
● Apple Safari
● Google Chrome
● Microsoft internet explorer

### ○ 2.4 Design and Implementation Constraints

```
● For the VMS system, the volunteers who are applying for the account must be at least 16
years of age.
● The size of the application should not exceed 50Mb for data transactions between the VMS
and BCS.
● The volunteer must not be able to see the information of the senior person until he or she is
assigned to them.
● The assignment process must not exceed more than 2 days.
● Volunteers must have only one assignment at one time.
```
### ○ 2.5 Assumptions and Dependencies

There are multiple assumptions that have to be made for the system to give the expected results.
For example, we need the police background check system which should be fully operational and
be able to return the results of the background checks within 48 hours. We would also need to
assume the people's engagement in beneficial activities like volunteering which will reduce the
crime rate in the city by 10% approximately. This will lead to the next assumption which is possible
sponsors like owners of local businesses will offer different promotions to the volunteers as
incentives. All of that is also very dependent on enough volunteers who can support the senior
people that will also have the minimum educational skills, pass the police certificate, and be
interested in participating. We have one main dependency which is the police certificate check
volunteers need to go through. We have to send all the data, and the government is in charge of
processing everything and returning a background check report.


## 3. Data Requirements

### 3.1 User Interfaces

### 3.1.1 User Profile


### 3.1.2 Service Requests Page

### ○

### 3.1.3 Volunteer approval page


## 4. System Features

### 4.1 Create new volunteer

```
Requirement
ID
```
```
Description
```
```
FR_01 The user shall be able to initiate the registration process
FR_02 The system shall be able open the form for volunteer
account creation.
```
```
FR_03 The candidate shall be able to enter his personal
information.
FR_04 The system shall be able to validate the candidates
personal information
```
```
FR_05 The system shall store the candidates’ personal
information, if the data format is valid
FR_06 The user shall be able to submit the application form
FR_07 The user shall be able to change his personal
information, if the data is not in a valid format.
FR_08 The system shall be able to send the candidates personal
information to the volunteer administrator.
FR_09 The system shall notify the candidate about his stage of
application, using email format.
```
### 4.2 Assign volunteer

```
Requirement
ID
```
```
Description
```
```
FR_01 The system shall display the list possible senior people
cases
FR_02 The system shall display the list of available volunteers
FR_03 The system shall display a list of interests of each of the
available volunteers.
FR_03 The system shall display the volunteering history for each
available volunteer
```

```
FR_04 The system shall display the scoring of the each available
volunteer of his previous assignments
FR_06 The volunteer administrator shall be able to assign the
volunteer to the senior person case
FR_07 The system shall notify the volunteer of the assignment
```
```
FR_08 The system shall receive assignment confirmation from the
volunteer.
FR_09 The system shall be able to confirm the assignment.
FR_10 The system shall store the assignment information
FR_10 The system shall notify administrator and SPCC employee,
if volunteer approves assignment
```
### 4.3 Generate Daily Report

```
Requirement
ID
```
```
Description
```
```
FR_01 The system shall download data from senior cases
FR_02 The system shall calculate predictions/ forecast based on
the data
FR_03 The system shall identify any missing data.
```
```
FR_04 If there is a complete data, the system shall generate a
report
FR_05 The system shall send the report to the volunteer
administrator
```
```
FR_06 The volunteer administrator shall be able to see the report
FR_07 The volunteer administrator shall be able to change the
report
FR_08 The volunteer administrator shall be able to confi rm the
report
FR_09 The system shall save the report
```

## 5. Other Nonfunctional Requirements

### 5.1 Performance Requirements

The system has to be very fast, easy to learn, and easy to use. The system should reduce the
volunteer assignment time to 30%. Also, the system should have a 0-4 second load time which in
other business is best for conversion rates, being the fi rst fi ve seconds of page-load time the ones
that have the highest impact on conversion rates, and in our case, translates to higher satisfaction
metrics and more users using the platform.

### 5.2 Safety Requirements

Parents don’t like to let kids use any application without their consent, so the system should be able
to prevent students or minors from having an account in this application. Age and identity should be
verified prior to enabling access to all the features and functionalities of the platform.

### 5.3 Security Requirements

Only the data that was generated less than 2 years ago should be stored and kept only for the
purpose of generating reports and basic platform operation but should never be shared with third
parties for different motives without prior explicit consent. System should also be able to only allow
assigned volunteers to see the data of the assigned cases. Volunteers should not have global access
to the rest of the cases and people in the platform

### 5.4 Software Quality Attributes

Senior people should get volunteer services within three days. The volunteer management system
also has to send information to the background check system. The Volunteer Management System
should reduce the possibility of downtime to less than two times per year. Employees at the SPCC
will get all seniors' data over the phone, and the employees should be able to create profi les for the
senior people on the VMS.


## 6. Other Requirements

## Appendix A: Glossary

```
Data Element Description Composition or
Data Type
```
```
Length Values
```
```
Volunteer The person who will
apply to for the
volunteer account and
provide volunteering
services
```
```
Volunteer ID
● First name
● Last name
● DOB
● Address
```
```
Volunteer ID Unique identifier for
each volunteer
```
```
Integer 8 System generated
sequential integer,
beginning with 1.
First name The name of the
volunteer who provides
services.
```
```
Alphabetic characters 30 Cannot contain blanks
```
```
Last Name The last name of the
volunteer who provides
services
```
```
Alphabetic characters 30 Cannot contain blanks
```
```
DOB The birthday of the
volunteer who provides
services
```
```
Date Records the time
using ISO 8601 date
format with
milliseconds.
Address The location of the
volunteer
```
```
Alphabetic characters 40 Cannot contain blanks
```
```
Admin The person who
manages and checks
volunteers and
monitors senior people.
The main action of this
person is assignment
creation.
```
```
Admin ID
● First name
● Last name
```
```
Admin ID Unique identifier for
each admin
```
```
Integer 8 System generated
sequential integer,
beginning with 1.
```

First name The name of the admin Alphabetic characters 30 Cannot contain blanks

Last Name The last name admin Alphabetic characters 30 Cannot contain blanks

Account
application

```
Request for a new
Volunteer account
```
```
Application ID
+VolunteerID
+ Application status
```
Application ID unique identifier for the
application.

```
Integer 8 System generated
sequential integer,
beginning with 1.
```
Volunteer ID Reference to the
Volunteer ID from
volunteer entity

```
Integer 8 Can contain only
those values that are
in the Volunteer entity
```
Senior The person who
receives the services

```
Senior ID
● First name
● Last name
● DOB
● Address
```
Senior ID Unique identifier for
each senior person

```
Integer 8 System generated
sequential integer,
beginning with 1.
```
Assignment
/Service

```
Specific Volunteer
provides the service to
the specific senior
person.
```
```
Assignment ID
● Volunteer ID
● Senior ID
● Assignment
date
+ Admin ID
```
Assignment
ID

```
Unique identifier for
each assignment
```
```
Integer 8 System generated
sequential integer,
beginning with 1.
```
Volunteer ID Reference to the
Volunteer ID from
volunteer entity

```
Integer 8 Can contain only
those values that are
in the Volunteer entity
```
Senior ID Reference to the Senior
ID from senior entity

```
Integer 8 Can contain only
those values that are
in the Senior entity
```
Admin ID Reference to the Admin
ID from admin entity

```
Integer 8 Can contain only
those values that are
in the Admin entity
```

Assignment
date

```
The date when the
assignment was made
by the admin
```
```
Date The value contain
present or past dates
```
Feedback The feedback senior
person gives to the
volunteer after
assignment is
completed

```
Feedback ID
● Volunteer ID
● Senior ID
● Assignment ID
● Text
```
Feedback ID Unique identifier for
each feedback given by
senior person

```
Integer 8 System generated
sequential integer,
beginning with 1.
```
Text The text that contains
senior’s feedback

```
Alphabetic characters 250 Can contain blanks
```
BCS The police background
check system that
process the volunteers’
information

```
Police ID
● Application ID
● Check date
```
Police ID Unique identifier for
the each police officer

```
Integer 8 System generated
sequential integer,
beginning with 1.
```
Application ID Reference to the
application ID from the
account application
status

```
Integer 8 Can contain the value
only which is on
account application
status
```
Check date The time when the
application is being
checked

```
Date The value contain
present and past dates
```

## Appendix B: Analysis Models

```
Relative Weight 2 1 0. 5 1
```
```
Features RBeelnaetifivte RPeelnaatlitvye Tvaoltuael Value % RcoelsattiveCost % Rrieslkative Risk % Priority
```
```
1 Create senior-peer volunteer 9 9 27 25. 96 % 7 20. 59 % 9 34. 62 % 0. 58
```
```
2 Create student-peer volunteer 1 1 3 2. 88 % 7 20. 59 % 9 34. 62 % 0.
```
```
3 Assign volunteer 9 9 27 25. 96 % 7 20. 59 % 1 3. 85 % 1. 84
```
```
4 Generate daily report 5 9 19 18. 27 % 7 20. 59 % 5 19. 23 % 0. 62
```
```
5 Record volunteer progress report 7 3 17 16. 35 % 5 14. 71 % 1 3. 85 % 1. 46
```
```
6 Modify volunteer data 3 5 11 10. 58 % 1 2. 94 % 1 3. 85 % 1. 99
```
```
Totals 34 36 104 100. 00 % 34
```
```
100. 00
% 26100. 00 %
```
