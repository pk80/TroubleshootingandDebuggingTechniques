# Troubleshooting and Debugging Techniques

<!-- TOC -->
* [Troubleshooting and Debugging Techniques](#troubleshooting-and-debugging-techniques)
* [MODULE 1 : Troubleshooting Concepts](#module-1--troubleshooting-concepts)
  * [Introduction](#introduction)
  * [Introduction to Debugging](#introduction-to-debugging)
    * [Debugging](#debugging)
    * [Problem solving steps](#problem-solving-steps)
    * [Silently crashing application](#silently-crashing-application)
  * [Understanding Problem](#understanding-problem)
    * [It Doesn't Work](#it-doesnt-work)
    * [Creating a Reproduction Case](#creating-a-reproduction-case)
    * [Finding the Root Cause](#finding-the-root-cause)
    * [Dealing with Intermittent Issues](#dealing-with-intermittent-issues)
    * [Intermittently Failing Script](#intermittently-failing-script)
  * [Binary Searching a Problem](#binary-searching-a-problem)
    * [Binary Search](#binary-search)
    * [Linear and Binary](#linear-and-binary)
    * [Applying binary search in troubleshooting](#applying-binary-search-in-troubleshooting)
    * [Finding invalid data](#finding-invalid-data)
  * [Review](#review)
    * [Glossary : Course-4_Module-1](#glossary--course-4_module-1)
    * [Qwiklabs Assessment : Debug Python Scripts](#qwiklabs-assessment--debug-python-scripts)
* [MODULE 2 : Slowness](#module-2--slowness)
  * [Understanding Slowness](#understanding-slowness)
    * [Introduction to Slowness](#introduction-to-slowness)
    * [Why is my computer slow?](#why-is-my-computer-slow)
    * [How computers use resources](#how-computers-use-resources)
    * [Possible causes of slowness](#possible-causes-of-slowness)
    * [Slow web server](#slow-web-server)
    * [Monitoring tools](#monitoring-tools)
  * [Slow Code](#slow-code)
    * [Writing efficient code](#writing-efficient-code)
    * [Using the right data structures](#using-the-right-data-structures)
    * [Expensive loops](#expensive-loops)
    * [Keeping local results](#keeping-local-results)
    * [Slow script with expensive loop](#slow-script-with-expensive-loop)
    * [More about improving our code](#more-about-improving-our-code)
  * [When Slowness Problems Get Complex](#when-slowness-problems-get-complex)
    * [Parallelizing operations](#parallelizing-operations)
    * [Slowly growing in complexity](#slowly-growing-in-complexity)
    * [Dealing with complex slow systems](#dealing-with-complex-slow-systems)
    * [Using threads to make things go faster](#using-threads-to-make-things-go-faster)
    * [More about complex slow systems](#more-about-complex-slow-systems)
  * [Review](#review-1)
    * [Glossary : Course-4_Module-2](#glossary--course-4_module-2)
    * [Qwiklabs Assessment : Performance tuning in Python scripts](#qwiklabs-assessment--performance-tuning-in-python-scripts)
* [MODULE 3 : Crashing Programs](#module-3--crashing-programs)
  * [Why Programs Crash](#why-programs-crash)
    * [Introduction to Crashing Programs](#introduction-to-crashing-programs)
    * [Systems that Crash](#systems-that-crash)
    * [Understanding crashing applications](#understanding-crashing-applications)
    * [What to do when you can't fix the program?](#what-to-do-when-you-cant-fix-the-program)
    * [Internal server error](#internal-server-error)
    * [Resources for understanding crashes](#resources-for-understanding-crashes)
  * [Code that Crashes](#code-that-crashes)
    * [Accessing invalid memory](#accessing-invalid-memory)
    * [Unhandled errors and exceptions](#unhandled-errors-and-exceptions)
    * [Fixing someone else's code](#fixing-someone-elses-code)
    * [Debugging a segmentation fault](#debugging-a-segmentation-fault)
    * [Debugging a Python crash](#debugging-a-python-crash)
    * [Debugging with print](#debugging-with-print)
    * [Debugging with assert](#debugging-with-assert)
    * [Try and catch debugging](#try-and-catch-debugging)
    * [Python logging module](#python-logging-module)
    * [Python debugging with pdb](#python-debugging-with-pdb)
    * [Debugging/breakpoints in VS Code](#debuggingbreakpoints-in-vs-code)
    * [AI infused debugging and paired programming](#ai-infused-debugging-and-paired-programming)
    * [Resources for debugging crashes](#resources-for-debugging-crashes)
  * [Handling Bigger incidents](#handling-bigger-incidents)
    * [Crashes in complex systems](#crashes-in-complex-systems)
    * [Communication and documentation during incidents](#communication-and-documentation-during-incidents)
    * [Writing effective postmortems](#writing-effective-postmortems)
  * [Review](#review-2)
    * [Glossary : Course-4_Module-3](#glossary--course-4_module-3)
    * [Qwiklabs Assessment : Fix errors in Python scripts](#qwiklabs-assessment--fix-errors-in-python-scripts)
* [MODULE 4 : Managing Resources](#module-4--managing-resources)
  * [Managing computer resources](#managing-computer-resources)
    * [Introduction on Managing Resources](#introduction-on-managing-resources)
    * [Memory leaks and how to prevent them](#memory-leaks-and-how-to-prevent-them)
    * [Managing disk space](#managing-disk-space)
    * [Network saturation](#network-saturation)
    * [Dealing with memory leaks](#dealing-with-memory-leaks)
    * [More about managing resources](#more-about-managing-resources)
  * [Managing our time](#managing-our-time)
    * [Getting to the important tasks](#getting-to-the-important-tasks)
    * [Prioritizing tasks](#prioritizing-tasks)
    * [Estimating the Time tasks will take](#estimating-the-time-tasks-will-take)
    * [Communicating expectations](#communicating-expectations)
    * [More about making the best use of your time](#more-about-making-the-best-use-of-your-time)
  * [Making our future live easier](#making-our-future-live-easier)
    * [Dealing with Hard Problems](#dealing-with-hard-problems)
    * [Proactive Practices](#proactive-practices)
    * [Planning Future Resource Usage](#planning-future-resource-usage)
    * [Change management in virtualized environments](#change-management-in-virtualized-environments)
    * [Containerized Applications : Docker](#containerized-applications--docker)
    * [Preventing Future Problems](#preventing-future-problems)
    * [More about preventing future breakage](#more-about-preventing-future-breakage)
  * [Review](#review-3)
    * [Glossary : Course-4_Module-4](#glossary--course-4_module-4)
    * [Qwiklabs Assessment : Debug and Solve Software Problems](#qwiklabs-assessment--debug-and-solve-software-problems)
    * [IT skills in action](#it-skills-in-action)
  * [Interviewing](#interviewing)
    * [Getting interviews through networking](#getting-interviews-through-networking)
    * [The interview process](#the-interview-process)
    * [Interviewing at different type of companies](#interviewing-at-different-type-of-companies)
    * [Developing an Elevator Pitch](#developing-an-elevator-pitch)
    * [Asking the interviewer questions](#asking-the-interviewer-questions)
    * [Answer questions with the STAR method](#answer-questions-with-the-star-method)
    * [Interview warmup](#interview-warmup)
    * [Negotiating the contract](#negotiating-the-contract)
  * [Wrap up](#wrap-up)
<!-- TOC -->

# MODULE 1 : Troubleshooting Concepts

##  Introduction
- Different flavors of technical problems
  - crashing unexpectedly
  - getting stuck when it should be processing information
  - make your script run faster, use less memory, or transmit less data over the network
  - overall system isn't running as expected
- We'll learn how to solve any technical problem 

##  Introduction to Debugging

###  Debugging

###  Problem solving steps

###  Silently crashing application

##  Understanding Problem

###  It Doesn't Work

###  Creating a Reproduction Case

###  Finding the Root Cause

###  Dealing with Intermittent Issues

###  Intermittently Failing Script

##  Binary Searching a Problem

###  Binary Search

###  Linear and Binary

###  Applying binary search in troubleshooting

###  Finding invalid data

##  Review

###  Glossary : Course-4_Module-1

###  Qwiklabs Assessment : Debug Python Scripts

# MODULE 2 : Slowness

##  Understanding Slowness

###  Introduction to Slowness

###  Why is my computer slow?

###  How computers use resources

###  Possible causes of slowness

###  Slow web server

###  Monitoring tools

##  Slow Code

###  Writing efficient code

###  Using the right data structures

###  Expensive loops

###  Keeping local results

###  Slow script with expensive loop

###  More about improving our code

##  When Slowness Problems Get Complex

###  Parallelizing operations

###  Slowly growing in complexity

###  Dealing with complex slow systems

###  Using threads to make things go faster

###  More about complex slow systems

##  Review

###  Glossary : Course-4_Module-2

###  Qwiklabs Assessment : Performance tuning in Python scripts

# MODULE 3 : Crashing Programs

##  Why Programs Crash

###  Introduction to Crashing Programs

###  Systems that Crash

###  Understanding crashing applications

###  What to do when you can't fix the program?

###  Internal server error

###  Resources for understanding crashes

##  Code that Crashes

###  Accessing invalid memory

###  Unhandled errors and exceptions

###  Fixing someone else's code

###  Debugging a segmentation fault

###  Debugging a Python crash

###  Debugging with print

###  Debugging with assert

###  Try and catch debugging

###  Python logging module

###  Python debugging with pdb

###  Debugging/breakpoints in VS Code

###  AI infused debugging and paired programming

###  Resources for debugging crashes

##  Handling Bigger incidents

###  Crashes in complex systems

###  Communication and documentation during incidents

###  Writing effective postmortems

##  Review

###  Glossary : Course-4_Module-3

###  Qwiklabs Assessment : Fix errors in Python scripts

# MODULE 4 : Managing Resources

##  Managing computer resources

###  Introduction on Managing Resources

###  Memory leaks and how to prevent them

###  Managing disk space

###  Network saturation

###  Dealing with memory leaks

###  More about managing resources

##  Managing our time

###  Getting to the important tasks

###  Prioritizing tasks

###  Estimating the Time tasks will take

###  Communicating expectations

###  More about making the best use of your time

##  Making our future live easier

###  Dealing with Hard Problems

###  Proactive Practices

###  Planning Future Resource Usage

###  Change management in virtualized environments

###  Containerized Applications : Docker

###  Preventing Future Problems

###  More about preventing future breakage

##  Review

###  Glossary : Course-4_Module-4

###  Qwiklabs Assessment : Debug and Solve Software Problems

###  IT skills in action

##  Interviewing

###  Getting interviews through networking

###  The interview process

###  Interviewing at different type of companies

###  Developing an Elevator Pitch

###  Asking the interviewer questions

###  Answer questions with the STAR method

###  Interview warmup

###  Negotiating the contract

##  Wrap up