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
        * [Qwiklab Assessment : Debug Python Scripts](#qwiklab-assessment--debug-python-scripts)
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
        * [Qwiklab Assessment : Performance tuning in Python scripts](#qwiklab-assessment--performance-tuning-in-python-scripts)
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
        * [Fixing someone else code](#fixing-someone-else-code)
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
        * [Qwiklab Assessment : Fix errors in Python scripts](#qwiklab-assessment--fix-errors-in-python-scripts)
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
        * [Qwiklab Assessment : Debug and Solve Software Problems](#qwiklab-assessment--debug-and-solve-software-problems)
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

## Introduction

- Different flavors of technical problems
    - crashing unexpectedly
    - getting stuck when it should be processing information
    - make your script run faster, use less memory, or transmit fewer(less) data over the network
    - overall system isn't running as expected
- We'll learn how to solve any technical problem
- Prerequisites for this course:
    - Operating Systems: file systems, processes, log files
    - Computer hardware: CPU, RAM, disk, graphic, and Network Cards
    - Basic Networking: network connections and network bandwidth

## Introduction to Debugging

- Essential debugging techniques
    - basic process that we can use for tackling any technical problem
    - different ways we can approach understanding
        - what's going on and
        - finding the root cause of an issue
        - including a process called binary search to troubleshoot problems.
    - how to apply techniques (reusable) to solve
- Finally, you'll be able to apply techniques to solve a technical issue

### Debugging

- Troubleshooting : The process of identifying, analyzing, and solving problems
    - When we're fixing problems in the system running the application
- Problems may be caused by hardware, OS, applications running on the computer, or environment and configuration of the
  software
- Debugging : The process fo identifying, analyzing, and removing bugs in a system
    - When we're fixing the bugs in the actual code of the application
- Tools to get more information about the system
    - `tcpdump` and `Wireshark` : show ongoing network connections
    - `ps`, `top` or `free` : show number and types of resources used in the system
    - `strace` : look at system calls made by a program
    - `ltrace` : look at library call made by the software
- Debuggers : Let us follow the code line by line, inspect changes in variable assignments, interrupt the program when a
  specific condition is met, and more

### Problem solving steps

1. Getting information
2. Finding the root cause
3. Performing the necessary remediation

### Silently crashing application

- reproduce the problem
- tools used to identify the problems
    - strace : shows all system calls and errors
- System calls : calls that the programs running on our computer make to the running kernel

```text
strace ./<executable_file>
strace -o failure_output.strace ./<executable_file>
less failure_output.strace
# trace the error and solve it
```

- document the issue
- immediate remediation is to tell the user how to solve the core problem
- long term remediation is to contact developers of the software and let them know about the issue

## Understanding Problem

### It Doesn't Work

- more information from the user who complains "it doesn't work"
    - what were you trying to do?
    - what steps did you follow?
    - what was the expected result?
    - what was the actual result?
- The load average on linux is how much time a processor is busy in a given minute, with one meaning it was busy for the
  whole minute. This shouldn't be above the amount of processors in the computer.
- A number higher than the amount of processors means teh computer is overloaded.
- Stop the backup system by calling kill-STOP. This will suspend the execution of the program until you let it continue
  or decide to terminate it.

### Creating a Reproduction Case

- Reproduction case : a way to verify if the problem is present or not
- look at logs :
    - linux : /var/log/syslog and .xsession-errors
    - mac-os : /Library/Logs
    - windows : Event viewer

### Finding the Root Cause

- understanding the root cause is essential for performing the long-term remediation.
- problem-solving (debugging) creativity
- different ideas until we find one that explains the problem
- look at information we currently have and gather more if needed
- searching online for error messages
- look at the documents of the applications involved
- check hypothesis in a test environment instead of production environment
- tools help you get more information
    - `iotop` : like `top`, lets us see which processes are using the most input and output
    - `iostat` : show statistics on the input/output operations and the virtual memory operations
    - `vmstat` : same as `iostat`
- `ionice`, command used to make our backup system reduce its priority to access the dist and let the web services use
  it too
- `iftop`, similar to `top` showing the current traffic on the network interfaces
- `rsync`, command used for backing up data, includes `-bwlimit` option
- `Trickle`, program to limit the bandwidth being used
- `nice`, command to reduce the priority of the process and accessing the CPU

### Dealing with Intermittent Issues

- Bugs that come and go are hard to reproduce, and are extremely annoying to debug
- Debug an issue
    - get more involved in what's going on
    - adding more logging information to the service around inputs and function calls
    - check for logging configuration
    - monitor the environment
- Depending on the problem, look at
    - the load on the computer
    - the processes running at the same time
    - the usage of the network
- Heisenbug issue : bug goes away when we add extra logging information or when we follow the code step by step using a
  debugger. This is an annoying type of intermittent issue.
- Werner Heisenberg : scientist first described the observer effect
- Observer Effect : observing a phenomenon alters the phenomenon
- another intermittent issue is when we go off and on

### Intermittently Failing Script

- Finding the root cause of the problem in sending meeting

## Binary Searching a Problem

### Binary Search

- Linear Search : longer list, longer it takes
- Binary Search : search on sorted list
    - calculated as the base two algorithm of lists length

### Linear and Binary

### Applying binary search in troubleshooting

### Finding invalid data

- `wc` command counts the characters, words and lines in a file
- `head` command prints the first lines in the file
- `tail` command prints the last lines in the file

```text
# Below is the bisect method
# print number of lines in a file
wc -l <filename>
# print first 15 lines in the file
head -15 <filename>
# print last 20 lines in the file
tail -20 <filename>
# finding in first half of the file
```

## Review

### Glossary : Course-4_Module-1

**Terms and definitions from Course 4, Module 1**

- **Binary search**: A search algorithm used to find a specific item in a sorted list or array by repeatedly dividing
  the
  search space in half until the desired item is found or determined to be absent
- **Bisecting**: Dividing in two, also a Git command
- **Debuggers**: Tools that follow the code line by line, inspect changes in variable assignments, interrupt the program
  when a specific condition is met, and more
- **Debugging**: The process of identifying, analyzing, and removing bugs in the actual code of a system in the
  application
- **Linear search**: The process of searching each line of data until the desired data entry is located
- **Observer effect**: The idea that observing a phenomenon alters the phenomenon
- **System calls**: The calls that the programs running on our computer make to the running kernel
- **Troubleshooting**: The process of solving any kind of problem in the system running the application

### Qwiklab Assessment : Debug Python Scripts

Imagine one of your colleagues has written a Python script that's failing to run correctly. They're asking for your help
to debug it. In this lab, you'll look into why the script is crashing and apply the problem-solving steps that we've
already learned to get information, find the root cause, and remediate the problem.

# MODULE 2 : Slowness

## Understanding Slowness

### Introduction to Slowness

- Reasons for slowness
    - computer
    - scripts
    - complex systems
    - opened applications

### Why is my computer slow?

- instructions allow seemingly execute number of things at the same time
- Addressing slowness / identifying bottleneck
    - device
    - script
    - system
    - other resource limiting the process
    - CPU, disk, memory or network
- Monitor the usage of each resource and then workout which one is blocking our programs to run faster
    - `top`, `iotop`,`iftop`
    - MacOS - Activity Monitor
    - Windows - Resources Monitor, Performance Monitor

### How computers use resources

- Transmission speed : CPU's internal memory > RAM > File in disk > Network
- Cache : Stores data in a form that's faster to access than its original form
- Memory leak : Memory which is no longer needed is not getting released

### Possible causes of slowness

### Slow web server

```text
# figure out how slow website is responding
ab -n 500 <website>/
...
# ab stands for Apache Benchmark tool
# 500 is the number of requests made to website
```

```text
# connecting to the web server
ssh webserver
password:.....
.....

# check for anything suspicious
top

# start a process with different priority : nice
nice 
# change priority of a process that's already running : use renice
for pid in $(pidof COMMAND); do renice 19 $pid; done
```

```text
ps ax | less
```

```text
for pid in $(pidof COMMAND); do while kill -CONT $pid; do sleep 1; done; done
ab n 500 <website>/
```

### Monitoring tools

## Slow Code

### Writing efficient code

- readable, easy to write & understand
- clear code and try to make it run faster
- trying to optimize every second out of a script is probably not worth your time
- if we want our code to finish faster, we need to make our computer do less work
- profiler : tool that measures the resources that our code is using, giving us a better understanding of what's going
  on
    - gprof : to analyse c program
    - cProfile : to analyse python program (to count function calls)
- expensive action : those that can take a long time to complete
    - include parsing a file, reading data over network or iterating through whole list

### Using the right data structures

- Lists, Dictionaries, Tuples, and Sets are important data structures in python
- Lists : sequence of elements.
    - we can add/remove/modify them
    - we can iterate through the whole list to operate on each of the elements
    - it's called as ArrayList in java, Vector in C++, Array in Ruby and Slice in Go
    - This takes more time to find something in the list if it is too long
    - if you need to access elements by position, or will always iterate through all the elements, use a list to them.
- Dictionaries : store key-value pairs.
    - we can add data by associating value to a key
    - we can retrieve a value by looking up a specific key
    - it's called as HashMap in Java, Unordered Map in C++, Hash in Ruby and Map in Go
    - superfast for looking up for keys in just for one operation
    - if you need to look up the element using a key, use a dictionary
- think twice about creating copies of structures that we have in memory (maybe big)

### Expensive loops

- loops make our computer do things repetitively
- if you do an expensive operation inside the loop, you multiply the time it takes to do the expensive operation by the
  amount of time you repeat the loop.
- it is better to do expensive operations outside the loop
- make sure that the list of elements that you're iterating through is only as long as you really need it to be
- remember to break out of the loop once you've finished what you were looking for

### Keeping local results

- avoid expensive operations by creating a local cache
- remember to update cache (once per day)
- sometimes creating a variable also suffice this purpose

### Slow script with expensive loop

- different values in the print on how long it took to execute a command by calling it with `time`
    - Real : the amount of actual time that it took to execute the command
        - this is sometimes called as wall-clock time
    - User : the time spent doing operations in the user space
    - Sys : the time spent doing system-level operations
- user profilers to get some data what's going on
    - `pprofile3 -f callgrind -o profile.out <command>`
        - -f flag is to use callgrind file format
    - `kcachegrind <profile.out>` to look at the contents, a graphical interface for looking into these files.

### More about improving our code

## When Slowness Problems Get Complex

### Parallelizing operations

- do operations in parallels
- `concurrency` is how we write programs that do operations in parallel
- best way to do this is to split them across different processes
- good balance of different work loads
- Threads : let us run parallel tasks inside a process
    - Asyncio module in python does this

### Slowly growing in complexity

### Dealing with complex slow systems

### Using threads to make things go faster

### More about complex slow systems

## Review

### Glossary : Course-4_Module-2

### Qwiklab Assessment : Performance tuning in Python scripts

# MODULE 3 : Crashing Programs

## Why Programs Crash

### Introduction to Crashing Programs

### Systems that Crash

### Understanding crashing applications

### What to do when you can't fix the program?

### Internal server error

### Resources for understanding crashes

## Code that Crashes

### Accessing invalid memory

### Unhandled errors and exceptions

### Fixing someone else code

### Debugging a segmentation fault

### Debugging a Python crash

### Debugging with print

### Debugging with assert

### Try and catch debugging

### Python logging module

### Python debugging with pdb

### Debugging/breakpoints in VS Code

### AI infused debugging and paired programming

### Resources for debugging crashes

## Handling Bigger incidents

### Crashes in complex systems

### Communication and documentation during incidents

### Writing effective postmortems

## Review

### Glossary : Course-4_Module-3

### Qwiklab Assessment : Fix errors in Python scripts

# MODULE 4 : Managing Resources

## Managing computer resources

### Introduction on Managing Resources

### Memory leaks and how to prevent them

### Managing disk space

### Network saturation

### Dealing with memory leaks

### More about managing resources

## Managing our time

### Getting to the important tasks

### Prioritizing tasks

### Estimating the Time tasks will take

### Communicating expectations

### More about making the best use of your time

## Making our future live easier

### Dealing with Hard Problems

### Proactive Practices

### Planning Future Resource Usage

### Change management in virtualized environments

### Containerized Applications : Docker

### Preventing Future Problems

### More about preventing future breakage

## Review

### Glossary : Course-4_Module-4

### Qwiklab Assessment : Debug and Solve Software Problems

### IT skills in action

## Interviewing

### Getting interviews through networking

### The interview process

### Interviewing at different type of companies

### Developing an Elevator Pitch

### Asking the interviewer questions

### Answer questions with the STAR method

### Interview warmup

### Negotiating the contract

## Wrap up