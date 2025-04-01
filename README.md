# Troubleshooting and Debugging Techniques

<!-- TOC -->

* [Troubleshooting and Debugging Techniques](#troubleshooting-and-debugging-techniques)
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
    * [Review](#review)
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

# MODULE 4 : Managing Resources

## Managing computer resources

### Introduction on Managing Resources

### Memory leaks and how to prevent them

- Memory leak :
    - happens when a chunk of memory that's no longer needed is not released
    - if it becomes larger, can cause the whole system to start misbehaving
    - causing unrelated programs to crash
- Garbage collector :
    - It is the in charge of freeing the memory that's no longer in use
- Use of memory profiler to figure out how the memory is being used
    - `Valgrind` for C and C++ programs
    - For python
        - `cProfile` (built-in for general performance analysis)
        - `line_profiler` (for line-by-line analysis)
        - `memory_profiler ` (for memory usage)
        - `py-spy` (for low-overhead, real-time profiling)
- When a function returns, variables, or dictionaries are not referenced, and the garbage collector gives back the
  memory is NOT a memory leak
- An app that still needs a lot of memory, even after a restart, most likely points to a memory leak. This is a possible
  memory leak

### Managing disk space
- Reasons for programs may need disk space
  - installed binaries and libraries
  - data stored by the applications
  - cached information
  - logs
  - temporary files
  - backups
 
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

### Qwiklabs Assessment : Debug and Solve Software Problems

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