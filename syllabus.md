---
layout: page
title: Syllabus
description: >-
    Course policies and information
---

# Syllabus
{:.no_toc}

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Bulletin description

This course will teach you how to organize the data used in computer programs so that manipulation of that data can be done efficiently on large problems and large data instances. Rather than learning to use the data structures found in the libraries of programming languages, you will be learning how those libraries are constructed, and why the items that are included in them are there (and why some are excluded).

## General course info

- Term: Summer session 2, 2024
- Department: COMP
- Course number: 210
- Section number: 001
- Website: [comp210ss2.github.io](https://comp210ss2.github.io)
- Time: MoTuWeThFr 1:15 PM - 2:45 PM
- Location: Sitterson Hall FB007

## Instructor info

- Name: Jesse Wei
    - You can call me Jesse
- Office: Sitterson Hall SN315
- Email: jesse@cs.unc.edu
- Website: [jessewei.dev](https://jessewei.dev)
<!-- TODO: how many -->
- Office hours: MoTuWeThFr 2:45 PM - 3:45 PM, or by appointment
- Zoom link: [https://unc.zoom.us/j/91817043425](https://unc.zoom.us/j/91817043425)
    - Though I don't antipicate using Zoom much, if at all

## Textbook

There is no required textbook, and we will primarily use the resources on this website. However, you may use the free and open-source data structures textbook found at [opendatastructures.org](https://opendatastructures.org).

## Resources

I will use Canvas for course announcements.

Assignments will be submitted to [Gradescope](https://gradescope.com). The course entry code is `Z3ZZEX`. We will use GitHub Classroom to manage programming assignments. A [GitHub](https://github.com) account is required, though you should already have one. Our GitHub organization is [comp210ss2](https://github.com/comp210ss2). This is where your assignment code will be, and code from lecture will be posted in [comp210ss2/lecture_code](https://github.com/comp210ss2/lecture_code).

We will use Piazza for class discussion. You should also use it for private communication with me via a private post (i.e., please use Piazza instead of emailing me directly). You should have received an invitation to Piazza in your UNC email (`onyen@unc.edu`), but if not, you can sign up at [piazza.com/unc/summer2024/comp210](https://piazza.com/unc/summer2024/comp210).

## Course description

This course will teach you how to organize the data used in computer programs so that manipulation of that data can be done efficiently on large problems and large data instances. Rather than learning to use the data structures found in the libraries of programming languages, you will be learning how those libraries are constructed, and why the items that are included in them are there (and why some are excluded).

## Target audience

This course is intended for people who already have some experience with programming, though not necessarily in Java. I assume you have already learned about the following basic programming concepts:

* primitive types (integers, real numbers, booleans)
* variables
* constants
* expressions
* assignments
* comments
* arrays
* loops
* procedures, functions, methods

The target audience for this course includes students intending to major in computer science and students with some programming experience who are interested in learning about formal computer science.

## Prerequisites

Prerequisites, COMP 110 and MATH 231; a grade of C or better is required in both prerequisite courses ; Pre- or corequisite, COMP 283 or MATH 381 or STOR 315.

## Goals and key learning objectives

1. You will gain familiarity with important categories of problems that are commonly encountered in software development and will learn what data organizations will allow practical and efficient solutions to those problems.
2. You will learn the basics of how to describe and analyze the performance and efficiency of your algorithms, and this will prepare you for upper level courses in algorithm analysis, such as COMP 550 (Algorithms and Analysis) and COMP 750 (Algorithm Analysis). You will also be better prepared to study higher-level areas where data structures covered in this class are heavily used: operating systems, networking, graphics, image processing, compilers, databases, and robotics, to name a few.
3. You will demonstrate the concepts you learn by encoding them in correct Java programs.
4. You will gain more proficiency in basic programming and in constructing larger programs.
5. You will gain the prerequisite knowledge for modern technical coding interviews.

## Course requirements

Students should attend all lectures and check the course website for announcements and updates. Students will be required to complete 10-15 programming assignments. There will be several quizzes (dates will be announced ahead of time) throughout the semester and a final exam.

As this is a summer course, students should expect to spend 3-4 hours of work per day on programming assignments and reviewing course material.

## Key dates

The final exam will be held on Tuesday, July 30, 2024, from 11:30 AM to 2:30 PM, per the [university's final exam schedule](https://summer.unc.edu/class-and-final-examination-schedules/). The location will be our normal classroom FB007.

<!-- TODO: -->
Dates for quizzes are to be determined and will be posted on the [schedule](schedule.md).

Programming assignment release and due dates will be posted on the [schedule](schedule.md).

## Grading criteria

* Quizzes: 40%
* Final exam: 20%
* Programming assignments: 35%
* Participation: 5%

Participation will be based on your participation in class and on [Piazza](https://piazza.com/unc/summer2024/comp210).

### Final exam replacement policy

If your final exam score exceeds a quiz score, I will replace one or two (depending on how many quizzes we have this semester) of the lowest quiz scores with your final exam score.

## Course policies

You get four "late days" in total during the semester. You may use a late day to submit a programming assignment after the deadline via Gradescope. You may only use late days in one-day increments (no partial late days), and you may use only one late day per assignment. If you submit an assignmnent late after running out of late days, you will receive no credit for the submission. Please submit your assignments on time and save your late days for extraordinary situations. Please contact me in advance if there are extenuating circumstances that may warrant an exception to this policy.

## Honor code

In order to do well in this course, you must come to your own individual understanding of the material. Collaboration is encouraged to a limited degree.

For general course concepts, I encourage you to collaborate with your classmates. You may also use any online resources.

For graded course content (assignments and assessments), collaboration with other students is not allowed. Additionally,

* For assignments, you may use any online resource except public source code (e.g., GitHub, GitLab) and cheating services (e.g., Chegg). You may not use AI (e.g., ChatGPT) to write code for the assignment. See [Code review test](#code-review-test).
* Quizzes are closed-everything (notes, laptop, internet, etc.) except one 8.5" x 11" cheat sheet (front and back) prepared before the quiz.
* Similarly, the final exam is closed-everything except up to eight 8.5" x 11" cheat sheets (front and back). Eight should be an extreme upper bound, and you should not feel like you have to use all eight.
* Quizzes and the final exam are in-person and proctored.

You are expected to follow the terms of the [UNC Honor Code](https://studentconduct.unc.edu/honor-system/). If you have any questions, please ask me.

### Code review test

I reserve the right to, at any time, ask you to submit to a “code review” test with me. I may ask you to meet to explain any line of code or decision made in your program that I deem suspicious or confusing. Thus, you should be able to comfortably explain why you (and you alone) wrote any single line of code in an assignment handed in for credit. Should you be unable to do so, you may be taken to honor court depending on the severity of the infraction.

## Course schedule

See schedule on course website.

## Feedback

If you have suggestions on how to improve the course, please let me know. You should use this [anonymous feedback form](https://forms.gle/do2UzGX6jh7P7N2E6). Your email will not be collected. If you want me to follow up with you, you may provide your name (optional). If you make a suggestion that I can act on while I have time to do so, I probably will.

## Attendance policy

University Policy: As stated in the University’s [Class Attendance Policy](https://catalog.unc.edu/policies-procedures/attendance-grading-examination/), no right or privilege exists that permits a student to be absent from any class meetings, except for these University Approved Absences:

1. Authorized University activities: [University Approved Absence Office (UAAO) website](https://uaao.unc.edu/) provides information and [FAQs for students](https://uaao.unc.edu/faqs-for-students/) and [FAQs for faculty](https://uaao.unc.edu/faqs-for-faculty) related to University Approved Absences
2. Disability/religious observance/pregnancy, as required by law and approved by [Accessibility Resources and Service](https://ars.unc.edu) and/or the [Equal Opportunity and Compliance Office](https://eoc.unc.edu/accommodations/) (EOC)
3. Significant health condition and/or personal/family emergency as approved by the [Office of the Dean of Students](https://dos.unc.edu/), [Gender Violence Service Coordinators](https://vpas.unc.edu/confidential-support/), and/or the [Equal Opportunity and Compliance Office](https://eoc.unc.edu/) (EOC).

## Syllabus changes

I reserve the right to make changes to the syllabus, including assignment due dates and quiz dates. These changes will be announced as early as possible.

## Accessibility resources and service

[Accessibility Resources and Service](https://eoc.unc.edu/accommodations/) (ARS – [ars@unc.edu](mailto:ars@unc.edu)) receives requests for accommodations, and through the Student and Applicant Accommodations Policy determines eligibility and identifies reasonable accommodations for students with disabilities and/or chronic medical conditions to mitigate or remove the barriers experienced in accessing University courses, programs and activities.

ARS also offers its Testing Center resources to students and instructors to facilitate the implementation of testing accommodations.

## Counseling and psychological services

UNC-Chapel Hill is strongly committed to addressing the mental health needs of a diverse student body. The [Heels Care Network](https://care.unc.edu/) website is a place to access the many mental health resources at Carolina. CAPS is the primary mental health provider for students, offering timely access to consultation and connection to clinically appropriate services. Go to their website [https://caps.unc.edu/](https://caps.unc.edu) or visit their facilities on the third floor of the Campus Health building for an initial evaluation to learn more. Students can also call CAPS 24/7 at 919-966-3658 for immediate assistance.

## Title IX and related resources

Any student who is impacted by discrimination, harassment, interpersonal (relationship) violence, sexual violence, sexual exploitation, or stalking is encouraged to seek resources on campus or in the community. Reports can be made online to the EOC at [https://eoc.unc.edu/report-an-incident/](https://eoc.unc.edu/report-an-incident/) or by contacting the University’s Title IX Coordinator (Elizabeth Hall, [titleixcoordinator@unc.edu](mailto:titleixcoordinator@unc.edu)) or the Report and Response Coordinators in the Equal Opportunity and Compliance Office ([reportandresponse@unc.edu](mailto:reportandresponse@unc.edu)). Confidential resources include Counseling and Psychological Services and the Gender Violence Services Coordinators ([gvsc@unc.edu](mailto:gvsc@unc.edu)). Additional resources are available at [safe.unc.edu](https://safe.unc.edu).
