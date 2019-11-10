---
title: Governance
---

## Catalyst
_IBM Cloud Garage Catalyst_ (aka Catalyst) is an organized effort managed by IBM Cloud Garage to help development teams build and deliver cloud-natvie solutions deployed to IBM Cloud with Kubernetes and OpenShift.

<AnchorLinks>

- [Assets and projects](#assets-and-projects)
- [Roles and responsibilities](#roles-and-responsibilities)
- [Types of teams](#types-of-teams)
- [Governance](#governance)
- [Initial project teams](#initial-project-teams)

</AnchorLinks>

## Assets and projects

### Catalyst assets

_Catalyst assets_ (aka assets) are guidelines, components, and tooling, the result of community contributions of code, design, ideas, and guidance, that have been packaged and shared for reuse on development projects. Their purpose is twofold:
- Increase the productivity of application developers
- Increase the consistency of applications that are developed

Assets will embody best practices for common application architectures, implementations, and development tasks and make those best practices easier to apply. Assets will be managed and made available for use via projects.

### Catalyst projects

_Catalyst projects_ (aka projects) are open source efforts narrowly focused on specific areas of interest. The assets are divided into projects. A project should organize a set of related assets such that a user or contributor interested in a project should be interested in  all of the assets in a project.

Each project will store its assets in a GitHub repository to facilitate managing development of the assets as well as helping individual development projects to access and apply the assets.

## Roles and responsibilities

### Consumers

_Consumers_ are members of the community who are applying assets to their development projects. Anyone who wants to apply any of the assets can be a user. We encourage consumers to participate as evangelists and contributors as well.

### Evangelists

_Evangelists_ are members of the community who help others become consumers of the assets. They do so by:
- Advertising the assets and encouraging others to use them 
- Supporting new consumers and answering questions, such as on Slack (IBM internal)
- Reporting bugs or missing features through GitHub issues

### Contributors

_Contributors_ are members of the community who help maintain, improve, and expand the assets. In addition to using and evangilizing the assets, they make the assets better by:
- Resolving issues in GitHub to fix bugs, add features, and improve documentation 
- Submitting changes as GitHub pull requests

### Maintainers

_Project maintainers_ (aka maintainers) are owners of the project who are committed to the success of the assets in that project. Each project has a team of maintainers, and each team has a lead. In addition to their participation as contributors, maintainers have privileges to:
- Label, close, and manage GitHub issues
- Close and merge GitHub pull requests
- Nominate and vote on new maintainers

## Types of teams

### Core team

Core team members are IBM employees responsible for the leadership and strategic direction of the set of Catalyst projects as a whole. The core team also directs how the Catalyst strategy will evolve with IBM Cloud product decisions. Core team responsibilities include:

- Actively engaging with the projects' communities
- Setting overall direction and vision
- Setting priorities and release schedule
- Focusing on broad, cross-cutting concerns
- Spinning up or shutting down project teams

The core team will opperate the technical steering commottee.

#### Technical steering committee

The technical steering committee coordinates the project teams to ensure consistency between the projects and fosters collaboration between the core team and each project team. This close communication on cross-cutting concerns greatly mitigates the risk of misalignment that can come from decentralized efforts. The committee consists of the project leads of all of the projects as well as other members of the core team who may not presently be leading any projects.

### Project teams

Each project team maintains the assets in its project. Therefore, its members are the maintainers of the assets. Each project operates independently, though it should follow this governance structure to define roles, responsibilities, and decision-making protocols.

The project has a project lead, a lead maintainer who should also be a member of the [technical steering committee](#technical-steering-committee).

Each project lead is responsible for:
- Acting as a point of primary contact for the team
- Participating in the technical steering committee
- Deciding on the initial membership of project maintainers (in consultation with the core team)
- Determining and publishing project team policies and mechanics, including the way maintainers join and leave the team (which should be based on team consensus)
- Communicating core vision to the team
- Ensuring that issues and pull requests progress at a reasonable rate
- Making final decisions in cases where the team is unable to reach consensus (should be rare)

The way that project teams communicate internally and externally is left to each team, but:
- Technical discussion should take place in the public domain as much as possible, ideally in GitHub issues and pull requests.
- Each project should have a dedicated Slack channel (IBM internal). Decisions from Slack discussions should be captured in GitHub issues.
- Project teams should actively seek out discussion and input from stakeholders who are not members of the team.

## Governance

### Planning

Project planning is managed in a [Kanban board](https://en.wikipedia.org/wiki/Kanban_board), specifically this Zenhub board:

- [Planning Zenhub](https://github.ibm.com/garage-catalyst/planning)

### Decision-making

Project teams should use [consensus decision making](#consensus) as much as possible, but resort to [lack of consensus decision making](#lack-of-consensus) when necessary.

#### Consensus

Project teams use [consensus decision-making](http://en.wikipedia.org/wiki/Consensus_decision-making) with the premise that a successful outcome is not where one side of a debate has "won," but rather where concerns from _all_ sides have been addressed in some way. **This emphatically does not mean design by committee, nor compromised design.** Rather, it's a recognition that every design or implementation choice carries a trade-off and numerous costs. There is seldom a 100% right answer.

Breakthrough thinking sometimes end up changing the playing field by eliminating tradeoffs altogether, but more often, difficult decisions have to be made. **The key is to have a clear vision and set of values and priorities**, which is the core team's responsibility to set and communicate, and the project teams' responsibility to act upon.

Whenever possible, seek to reach consensus through discussion and design iteration. Concretely, the steps are:

- New GitHub issue or pull request is created with initial analysis of tradeoffs.
- Comments reveal additional drawbacks, problems, or tradeoffs.
- The issue or pull request is revised to address comments, often by improving the design or implementation.
- Repeat above until "major objections" are fully addressed, or it's clear that there is a fundamental choice to be made.

Consensus is reached when most people are left with only "minor" objections. While they might choose the tradeoffs slightly differently, they do not feel a strong need to _actively block_ the issue or pull request from progressing.

One important question is: consensus among which people, exactly? Of course, the broader the consensus, the better. When a decision in a project team affects other teams (e.g. new/changed API), the team will be encouraged to invite people (e.g. leads) from affected teams. But at the very least, **consensus within the members of the project team should be the norm for most decisions**. If the core team has done its job of communicating the values and priorities, it should be possible to fit the debate about the issue into that framework and reach a fairly clear outcome.

#### Lack of consensus

In some cases, though, consensus cannot be reached. These cases tend to split into two very different camps:

- **"Trivial" reasons**, e.g., there is not widespread agreement about naming, but there is consensus about the substance.
- **"Deep" reasons**, e.g., the design fundamentally improves one set of concerns at the expense of another, and people on both sides feel strongly about it.

In either case, an alternative form of decision-making is needed.

- For the "trivial" case, the project lead will make an executive decision or defer the decision to another maintainer on the team.
- For the "deep" case, the project lead is empowered to make a final decision, but should consult with the core team before doing so.

### Contribution process

Catalyst assets are typically stored in GitHub repositories and use a [fork and pull request](https://guides.github.com/activities/forking/) workflow for contributions. Specific instructions can be found in each project's GitHub `CONTRIBUTING.md` file.

### Contributor License Agreement

We require contributors outside of IBM to sign our Contributor License Agreement (CLA) before code contributions can be reviewed and merged. If you have questions, please [contact the core team](/help/support#email).

### Support

Have questions? Found a bug? Learn where to go and what to do by visiting the [Support page](/help/support).

## Initial project teams

The project teams are organized within three main areas of focus:
1. [Iteration Zero](#iteration-zero)
1. [Activation](#activation)
1. [Starter Kits](#starter-kits)

#### Iteration Zero

Iteration Zero helps a development project team quickly and easily create a consistent development environment that will support their cloud-native development needs, including deploying to Kubernetes and OpenShift.

There are currently two Iteration Zero projects:
- [CLI Tools Image](https://github.ibm.com/garage-catalyst/client-tools-image) -- A Docker image with the IBM Cloud SDK tools already installed
- [Iteration Zero Tools](https://github.ibm.com/garage-catalyst/iteration-zero-terraform) -- A set of scripts to create a software-defined project development environment

#### Activation

Activation helps ensure that development teams have the necessary skills. It will help developers grow compentency in key IBM Cloud Garage Method practices such as [TDD](https://www.ibm.com/cloud/garage/practices/code/practice_test_driven_development/), [contract-driven testing](https://www.ibm.com/cloud/garage/practices/code/contract-driven-testing), [continuous integration](https://www.ibm.com/cloud/garage/practices/code/practice_continuous_integration/), etc.

We call the activitation material the _Training Manual_. The manual is defined in these projects:
- [Student Material](https://github.ibm.com/garage-catalyst/training-manual-student) -- Generated PDFs of the training manual
- [Exercises](https://github.ibm.com/garage-catalyst/training-manual-exercises) -- Generated PDFs of the training manual exercises
- [Instructor Material](https://github.ibm.com/garage-catalyst/training-manual-instructor) -- Generated PDFs of the training manual, including instructions for the teacher
- [Training Manual Material](https://github.ibm.com/garage-catalyst/training-manual-material) -- Raw content for the training manual and scripts to build it into PDFs

#### Starter Kits

Starter Kits are sets of robust starter code to accelerate the project inception and initial architectural decisions

Starter Kits are broken into architectural areas

##### Microservices Architecture

![Starter Kits](./images/starterkits.png "Stater Kits")

##### Web Apps

##### Mobile

##### Backend for Frontend (BFF)

##### Microservices

- [Spring Boot Java Microservice](https://github.ibm.com/garage-catalyst/template-spring-boot)

#### Garage Method Content

TBD



