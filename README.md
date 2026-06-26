[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/bavo-YO-)
# CSCI 3540U Independent Study Project

## Student Information

Please add the names and GitHub usernames of all group members, as of the time of project submission, to the table below.  If you have fewer than 5 members, you may delete the extra row(s).

| #  | Full Name            | GitHub Username |
| -- | -------------------- | --------------- |
| 1  | Vedant Trivedi       | vednat123       |
| 2  | Muneeb Bhatti        | Muneeb312       |
| 3  | Smit Kalathia        | Smitkalathia    |


## Overview

Students will organize into groups (3-5 students per group), research a topic (a type of vulnerability) outside of the lecture content, and will create and solve a set of challenges related to that topic.

The marked components of this project are as follows:

1. Create a set of three challenges that include the vulnerability that you have selected, and deploy them to our CTF server:
2. Collaborate to create a write-up for your level 1 and level 2 challenges
3. Perform peer evaluation of the challenges for at least 2 other groups
4. Collaboratively create a presentation video about the vulnerability

## How to Sign Up

To ensure that all groups cover a unique topic, we'll be using a [sign-up form](https://forms.gle/foSxqc8ek99ATcwY6). If a topic is already taken by another group, you will be asked to choose another topic. Topics should go beyond what we learned in class, but they do not need to be a fully new topic. A new aspect to a topic that was covered is acceptable, but exactly the same topic is not. Similarly, your presentation should cover something different than what we learned directly in the lectures, and it should be directly related to software security.

[A live spreadsheet of already picked topics](https://docs.google.com/spreadsheets/d/1cvQfTySUAv5CE8epgd44zD_N3v8XGVJFYgPewhKhY00) is available.  Be sure to check this spreadsheet before you choose your topic.  Topics are first come, first served.

You can sign up your team now, and add your challenge topic at a later time.

## Topic Ideas

The following are some topic ideas that go beyond the course content:

- binary exploitation for any platform other than x86/x64
- reverse engineering for any platform other than x86/x64 and Android
- game hacking
- game anti-cheat
- any active directory attack
- any SMB attack
- LDAP injection
- command injection
- ransomware and malware
- LLM pentesting
- privilege escalation in Linux, Windows, MacOS, BSD, or other
- clickjacking
- client side template injection
- content security policy bypass
- cross-origin resource sharing bypass
- Java Web Tokens
- XML external entity attacks
- redis attacks
- OAuth attacks
- antivirus bypass
- persistence
- pivoting
- attacking password managers
- attacking encryption
- hacking IoT devices and/or protocols
- pentesting iOS apps and devices
- content management systems (e.g. Wordpress, Drupal)

Be sure to pick a topic where you know how to proceed.  You are expected to research the vulerability, and come up with ideas for the challenges, on your own.

There are likely many other examples, so do not consider this a comprehensive list.  If you have a different idea, run it by the instructor.

## Detailed Requirements

### Challenges

In your GitHub repository, you will create a directory, `challenges`, where you will include three challenges, each in their own directory:

`level1` - no protections will be in place
`level2` - some limited protections will be in place, but should be bypassable
`level3` - protections (this version of the app should not be vulnerable)

The apps will otherwise be the same application.  Be sure to use a vulnerability that is different from the ones that were covered in the lectures and/or the labs in this course.  Furthermore, try to branch out and use a different use case then examples that we had during the class.

_**Note:** You will be rewarded if your challenge is more like a medium or hard difficulty, rather than a trivial problem to solve._

_**Note:** No projects should require a great deal of configuration or deployment.  Your project should be ready to do, e.g. with a single command._

#### Web-based Challenge

If you choose to create a web application for your challenge, you will need to include everything required in order to run your web application in Docker.  If you are new to Docker, here are some basic instructions on [how to use Docker to deploy your web application](https://www.docker.com/blog/docker-for-web-developers/).  Place all required files to deploy your application within your challenge directory, and include a `HOW_TO_RUN.md` which includes the docker command to execute your web application.  This file should not be big, as only the docker command should be required.

_**Note:** Definitely, try to clone the repository on a fresh virtual machine, and run it in docker to verify that this deployment will work._

#### Binary Challenge

If your challenge is based on a compiled binary, simply include the resulting binary, a description of the platform required to execute that binary, and the source code used.  For example, you could use the following format:

`PLATFORM.md` - describe the platform requirements (e.g. Linux, amd64, libraries required)
`/bin` - contains your binary
`/src` - contains the source code
`Makefile` - the makefile to build your code

_**Note:** Using another build tool is acceptable, but be sure that it is obvious how to use it._

#### Reverse Engineering Challenge

If your challenge is related to reverse engineering, some of the requirements might not match exactly.  For example, you might not implement protections for `level2`, but you could create an application that has some measures taken that make reverse engineering more difficult.  You must still include both the binary (or deployed app) and the original source code.

A sample directory structure (in the case of a binary to be reverse engineered) is given below:

`PLATFORM.md` - describe the platform requirements (e.g. Linux, amd64, libraries required)
`/bin` - contains your binary
`/src` - contains the source code
`Makefile` - the makefile to build your code

_**Note:** Using another build tool is acceptable, but be sure that it is obvious how to use it._

#### Mobile Challenge

If your challenge is based on a compiled binary, simply include the resulting binary, a description of the platform required to execute that binary, and the source code used.  For example, you could use the following format:

`<your_app_name>.apk` - the final android package file to be deployed on a virtual or real device
`/project` - the Android Studio project, including the original source code

_**Note:** Be sure to have an appropriate `.gitignore` file to avoid unnecessarily large repositories._

#### Other Challenges

If your challenge doesn't match any of the examples above, such as a game hacking challenge, be sure to contact the instructor to verify that your challenge will be accepted.  The format of submission may differ, depending on the nature of the challenge.

### Write-ups

In your GitHub repository, you will create a directory, `writeups`, where you will include two write-ups, each in their own directory:

Since the `level3` challenge should be fully protected, there should be no way to exploit the vulnerability.  However, since `level1` and `level2` are vulnerable, a write-up should be created for each which describes the process used to test and exploit the application.  Be sure to include actual commands and their output, as well as a brief explanation of the thought process.  You can include failed attempts as well, if those attempts makde sense as a next step but just happen to not find anything.

### Peer Evaluation

In addition to TA and instructor evaluation, your challenges and write-ups will be evaluated by your peers, and of course, that means that you will be evaluating the challenges and write-ups for other groups.  Each member of the group will be responsible for evaluating the challenges and write-ups for at least 2 other groups.  Peers will aim to provide constructive feedback to the groups, so that they could theoretically improve their challenges or write-ups.

### Presentation Video

In your GitHub repository, you will create a directory, `writeups`, where you will include a presentation video about their topic.  The presentation will be developed collaboratively by all members of the group, and will be limited to roughly 8 minutes per group.  The video will include of the following:

1. Introduction to the specific vulerability (or vulnerabilities) present in the challenge (~2 mins)
2. An overview of how to exploit this vulnerability (~2 mins)
3. A quick demonstration of exploitation of the vulnerability in your `level2` challenge (~2 mins)
4. A description of how to protect against this vulnerability (~2 mins)

Any slides or other materials should be made available, either by putting the files into the `presentation` folder, and/or by providing a link to them from a `PRESENTATION.md` file within that folder, as part of your submission.

_**Note:** Since all members of the group will be required to participate in this presentation, it makes sense that all of the challenges created by that team are part of the same category._

## Rubric

| Weight      | Component                     |
| ----------- | ----------------------------- |
|  5 marks    | Presentation                  |
|  3 marks    | `level1` challenge            |
|  3 marks    | `level2` challenge            |
|  3 marks    | `level3` challenge            |
|  4 marks    | `level1` write-up             |
|  4 marks    | `level2` write-up             |
|  3 marks    | Peer eval for 2+ other groups |

_**Note:** Git logs and source code will be examined to ensure that this work has been split evenly among the team members.  When the work done is pretty even between the team members, teams will be scored collectively and receive the same grade.  If the work done is substantially different, then team members will be given individual scores that reflect on their own contributions to the project.  Every member of the team should participate in every step of the project.  If you have some reason that the Github commit logs do not reflect the even distribution of work, please contact the instructor to let them know._
