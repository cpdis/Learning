---
_Title_: Software Development Process

_Author(s)_: Udacity

_Keywords_: software, engineering, software engineering, programming, udacity, code

_Website_: https://classroom.udacity.com/courses/ud805/

_Start_: 7/5/17

_End_: 
---

# Introduction and Overview
What were the major causes of the software crisis?
- Increasing product complexity 
- Slow programmer productivity growth
- Rising demand for software

Software development is taking an abstract idea in a persons head and making it into a concrete system on a computer. This is a very complex process made easier by software processes.
- Systematic
- Formal

Four main software processes:
- Waterfall
- Evolutionary prototyping
- Rational unified process (RUP)/Unified Software Process (USP)
- Agile

Software phases:
1. Requirements engineering
    - talk to the customer or whoever the system is for
2. Design
3. Implementation
4. Verificaition and validation
5. Maintenance

What is the software lifecycle?
- Sequence of decisions that determine the history of your software
- There are many ways in which you can make decisions
- It is important to understand which models are good for which situations
- Small projects are usually appropriate for agile
- Larger projects may require a more rigorous approach
- Criticality of the software plays an important role when choosing a model
- May use multiple lifecycle models within a single project
- The bottom line is that choosing the right lifecycle is of fundamental importance

## Requirements Engineering
The cost of error correction is least during the requirements stage of the process, therefore, it is wise to be thorough and find any problems at this stage.

- Elicitation
- Analysis
- Specificiation
- Validation
- Management

## Design
Software requirements are analyzed in order to produce a description of the internal structure and organization of the system. Serves as the basis of the construction of the actual system.

Design phase made up of 6 activities which correspond to 6 design products:
- Architectural design <--> System structure
- Abstract specification <--> Software specification
- Interface design <--> Interface specification
- Component design <--> Component specification
- Data structure <--> Data structure specification
- Algorithm design <--> Algorithm specification

## Implementation
Realizing the design of the system into an actual software system.

Four principles of implementation:
1. Reduction of complexity
2. Anticipation of diversity
3. Structuring for validation (design for testability)
4. Use of (external) standards

## Verification and Validation
Checks that the software system meets its specification and fulfills its intended purpose. Validation: did we build the right system? Verification: did we build the system right?

## Maintenance
Once a software system has been released into the world, things might change and this requires maintenance.

Types of changes:
- Environment change
- Feature request
- Bug report
 
Types of maintenance:
- corrective
- perfective
- adaptive

Regression testing is the process of retesting your software after it has been modified to ensure that the changes made did not cause any bugs to occur.

## Software Process Model
A prescriptive model of what should happen from the beginning to end of a software project. It determines the order and establishes transition criteria.

1. Waterfall process
    - Software concept -> Requirements analysis -> architectural design -> detailed design -> coding and debugging -> system testing
    - Advantages
        - Find errors early
    - Disadvantages
        - Not flexible
2. Spiral process
    - Determine objectives -> Identify and resolve risks -> Development and test -> Plan the next iteration
    - Incremental, risk-oriented model
    - Advantages
        - Risk reduction
        - Functionality can be added later on
        - Software produced early
    - Disadvantages
        - Requires specific expertise
        - Complex
3. Evolutionary prototyping
    - Initial concept -> design and implement initial prototype -> refine prototype until acceptable -> complete and release prototype
    - Advantages
        - Immediate feedback
    - Disadvantages
        - Difficult to plan
        - Easy to slip into hacking something together
4. Rational Unified Process (RUP)
    - Works in an iterative way
    - Business modeling -> requirements -> analysis and design -> implementation test -> deployment
    - Inception -> Elaboration -> Construction -> Transition
5. Agile
    - Based on highly iterative and incremental development
    - Test driven development (TDD)
        - Write a test that fails -> Make only enough code for it to pass -> Improve code quality (refactor)

Choosing a software process model:
- requirements understanding
- expected lifetime
- risk
- schedule constraints
- interaction with management/customers
- expertise

Classic mistakes:
- People
    - heroics
        - too much emphasis on can-do attitudes
        - [mythical man month](https://en.wikipedia.org/wiki/The_Mythical_Man-Month)
    - work evironment
    - poor management
- Process
    - scheduling issues
    - planning issues
    - unforseen failures
- Product
    - gold plating
        - more requirements than needed
    - feature creep
        - average project has 25% more features than initially planned
    - research != development
- Technology
    - silver bullet syndrome
        - too much reliance on new technology
    - switching tools mid-development
    - no version control

# Version Control
A system that allows you to manage multiple revisions of the same information.

Why is VCS useful?
- Enforces discipline
- Archives versions
- Maintain historical information
- Enable collaboration
- Recover from accidental deletions or edits
- Conserve disk space

Don't add executable files or large files in version control system.

### Essential Actions
- Add
- Commit
- Update

Two main types:
- Centralized
- Decentralized

## Introduction to GIT
### GIT Workflow
- workspace (working directory)
    - modified
    - `git add` 
- index (stage)
    - staged
    - `git commit` to store in local repository
    - commit and add with `git commit -a`
    - `git diff` compares staging and working directory
- local repository (HEAD)
    - committed
    - `git push` pushes change to remote repository
    - `git diff HEAD` compares what is in the local repository (HEAD) and the working directory
- remote repository
    - `git clone` to create a local repository
    - `git fetch` gets files from remote and puts them in local repository (but not working directory)
    - `git merge` merges what is in the local repository (HEAD) with the working directory
    - `git pull` combines `git fetch` and `git merge`

`git branch` if you want to make changes or experiment without changing original files or project. `git branch myNewBranch` will create a new branch (separate from `master`). `git checkout -b myNewBranch` will do the same thing. `git merge` will merge the current branch with whatever other branch is specified (such as `master`). `git branch -d myNewBranch` will delete that `myNewBranch`. Switch to another branch with `git checkout myNewBranch`.