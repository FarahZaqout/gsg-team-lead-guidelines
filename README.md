# Team Lead Guidelines:
This is a set of general rules/notes to facilitate the work of team leads at the GSG Code Academy. All contributions and change suggestions are welcome.

## What is a team lead?
A team lead in the code academy takes both the roles of a software archetict and a team lead. Your job is to ensure the quality of the project while meeting the deadlines.

## What to expect from this experience:
As a team lead, you will face many challenges, ranging from deciding the best tools/archeticture to follow, to deciding how to split the work (pairs/solo).

**1- Unrealistic expectations:** 
As a team lead, your biggest concern will be the unrealistic expectation from both the PO and the team members. The PO is most likely going to be a non-technical person, and the team will most likely be excited enough to underestimate most tasks.

>As a team lead your responsibility is to scale down the scope of work to something you feel realistic and achievable within the deadline, keeping in mind the time it takes to allow for best practices and code refactoring.

***It's always better to underpromise and overdeliver rather than overpromise and underdeliver.***

**2- Unclear requirements:**
It is not uncommon to leave a meeting with the P.O with a clear picture of what you will be building, only to find it's not what the P.O really wanted. This is a tricky one since it comes from the team lead and the P.O both thinking they are on the same page when they are not.

> *  As a team lead, you should make sure you and the P.O are always on the same page. **Don't allow any room for assumptions**, no matter how obvious the feature/task might seem. 
> *  Ask as many question as u need (there are no stupid questions), and if you believe you have an accurate understanding of what the P.O wants, just **narrate your thoughts to them** to be 100% certain.


**3- Different code styles:**
This is a self learning course, and most of the students discover their own way to the same solution. While this is great, a side effect is that often times, each student has their own idea of how work should be done. Which isn't necessarily a bad thing.

>As a team lead, your responsibility is to ensure consistency of the code style, proper documentation and gitflow.

**4- Bugs:**
As is the case in most projects, you do not build the perfect solution. Students will most likely get things to work and then if they think it needs refactoring, they will refactor, and with the short period of development, testing usually takes the back seat. As a result, you will encounter a lot of bugs.
>As a team lead, your responsibility is to find the balance between perfect and broken. The application should be "good enough", meaning no major/breaking bugs should exist, otherwise, there should be room for tolerance. Afterall, that's what agile methodology is all about.

# Project Phases:
## 1- Design Phase:
The design sprint does not involve much coding. However, it is arguably the sprint that determines the quality of the product you are building.

Part of the design process includes validation of the concept, empathizing and generating a user journey, designing the user experience and user interface. This is very well structured in the Code Academy, so there's no need to go over it again.

The other part of the process is concerned with how to best map the process above to the coding side. This process includes:
 * Choosing the appropriate technologies.
 * Properly documenting the user journey and stories.
 * Splitting the projects into technical tasks.
 * Designing the structure of the app.

The points above are important to ensure smooth workflow, and help alot with eliminating a lot of would-be blockers and conflicts.

### Choosing the appropriate technologies:
There are a lot of technologies that help improve the quality of your work with the tech stack we use at the Code Academy (PostgreSQL, React.js, Node.js, Express.js).

When deciding on a technology to use keep in mind the following:
* Are we using any other new technologies? (You shouldn't learn more than one or two technologies at most). Sticking to what you know is also fine.
* Am I comfortable enough with this tech to handle any blockers in a reasonable amount of time?
* What are the advantages/disadvantages of the tech at hand? 
* Is it really a good fit for the task? Are there better solutions?
* Is it realistic to expect the students to learn how to use it in this project?
* Does it introduce any new concepts to the students? Are the new concepts going to be too much to handle?

When choosing a tech to use, you need the rest of your team to buy-in. You must not force your team to use it just because you like it. As long as they are able to use the core technologies (tech stack), then things are fine.

#### Examples of technology choices:
**Knex.js:**
* **Advantages:**
    * Got previous experience with it. Can reliably deal with most issues that the students will face. 
    * Easy query building for simple queries.
    * Reduces the chance of an SQL syntax error.
    * Easy and intuitive migrations. (usually a new concept).
* **Disadvantages:**
    * Inefficient for complex queries. (should not be a concern during the academy).
    * Moves the students away from practicing SQL. (This is a big one).

**Ant Design:**
* **Advantages:**
    * Large library that has most components one would need.
    * Easy to learn and use, supports react.
    * Saves a lot of time.

* **Disadvantages:**
    * Students get less practice with CSS.
    * Team lead must be prepared to modify the library in very particular cases. **(Rare, but it happens).**


These are examples of things the team lead should consider before deciding to use a technology.

### Properly Documenting the user stories:
Properly documented user stories allows us to easily figure out the technical tasks. This is important for rapid development with minimal refactoring and conflicts.

**What makes a good user story?**
There are many ways to write user stories, nobody seems to agree on the best one. But the point is to keep them specific such that each story describes a single interaction between the user and the app.

The team lead should start from the user journey, and break it down into a series of single interactions between the user and the app.

Writing user stories this way makes it very easy to plan the technical tasks accurately.


### Architecture:
Designing the archeticture of your app is about knowing in general how the data will flow across the app, which parts of the app communicate with which, and so on. This should be brainstormed with your team members, drawing the different parts of the app and figuring out how, when and why they should interact with each other.

### Splitting the project into technical tasks:
Techinical tasks should be strictly based on user stories. Generally speaking, a technical task should not relate more than one user story. However, multiple technical tasks can relate to the same user story.

Before you convert user stories into technical tasks, you should think about a few things.

#### **Scope of the Technical Tasks:**
Your technical tasks should always be consistent in terms of scope. A single technical task can sum up an entire story, or you can decide to further split it into frontend only and backend only issues.

> The smaller the scope the better it is to develop, track, review and debug the issue.

#### **API Documentation:**
What level of documentation is sufficient for your API? Is listing the endpoints and REST methods enough? Do I need to describe the shape of objects sent to/received from the API? Are there any environment variables needed?
At the very least, endpoints must be documented and should follow the same case style (camelCase only, kebab-case only...etc).

#### **Acceptance Criteria:**
Each technical issue should have distinct acceptance criteria. This is very important for teamwork and the review process.

#### **Basic setup requirements:**

Think about the things you need to deploy as soon as possible to start workin  and avoid having different PRs depen ing on each other. Thinks like epress server, database schema, react app and react router, as well as eslint, heroku and travis should be cleared out of the way before any work on the actual user stories begin. Other things might be needed too based on your app's archeticture.

#### **Time Estimates:**
Each issue should have a time estimate tied to it. This is very important for the students to gaugue their perception of their abilities as well as the complexity of any given task. It also helps determining what can be realistically done during the project period.

> Let the students estimate time by themselves, and then as a general rule, double their time estimates, unless you see otherwise. Don't hesitate to break this "rule". This is as much of an exercise for you as it is for the team.

#### **Use the Project Feature:**
The project feature is a great way to organize the issues you are going to work on each sprint.
You should generally have 5 main categories as follows:
* Backlog: this contains all the project's issues, regardless of priority.
* To-do: This should contain the issues you plan on delivering during the current sprint.
* In-progress: This should contain Issues that are being worked on. In general each member should have only one issue assigned to them in this category.
* Awaiting-review: Issues that are basically finished but require review.
* Done: This should contain issues which PRs have been approved, merged and closed.

The project feature allows you to easily go through issues, plan your sprint and track progress.

***A good design process means you will encounter the least possible amount of blockers and conflicts.***

---

## 2- Build Phase:
By this phase, all the team members should have very good understanding of what needs to be done and how.

### Add pre-commit hook:
[Pre commit](https://www.npmjs.com/package/pre-commit) is a great way to avoid wasting time on things like indentation, semi-colons...etc. This allows you to focus on the actual logic of the PR.

### Daily Checklist:
The first thing you should do at the beginning of the day is go over a few things:
* Check if there are multiple issues assigned to any given member.
* Check if there are issues still open after you have merged their PRs.
* Check that every team member is assigned an open issue.
* Check that every member has an open draft PR with in-progress label.

> If a team member is not pushing multiple commits each day, it means they are moving too slow, usually being stuck on something or trying different ways of doing something. 

### Reviewing PRs:
**PR Checklist:**
* Sufficient description: just by reading the description you should have a good idea what to expect in the PR.
* PRs must relate their respective issues.
* PR commits also should relate their respective issues.
* commits should be small, and their message should indicate what changes they bring.
* Good gitflow: A branch must always be created from the master branch. Otherwise, additional unnecessary files will make it super easy to get conflicts and make it near impossible to properly review the code.


>When reviewing a pull request keep in mind that different ways of doing the same thing can be all valid.
* [ ] At the moment a PR is open, check that it doesn't relate to too many issues and that it's going to be reasonably small and easy to handle for both you and the team. 
* [ ] Check that all the Acceptance criteria are fulfilled as described in the issue of the PR.
* [ ] Pull the branch locally for better review and debugging.
* [ ] Run the app locally and manually test each of the features as intended in the figma design and the user story.
* [ ] Check the separation of concerns in each PR.
* [ ] Check code abstraction, if a file has hundreds of line, it probably can be improved.
* [ ] Check that the style is consistent across the app.
    * es6 all the way or es5 all the way
    * async/await all the way, promises all the way or callbacks all the way (please no).
* [ ] Check that variable naming is descriptive.
* [ ] Check that they are not trying to reinvent the wheel. If they are not reusing their other team's code, or if what they are trying to do already has an existing library that is easy to use. (use your judgment on this one).
* [ ] Check code documentation, but take it easy on the students.
    * If the PR adds something major, it probably should be documented in the Repo's main `Readme.md`.
    * comments describe what a function does. (This is reasonable to require).
    * Use JSdocs if you see fit. (only if you think the students can handle it without significant drop in progress and learning).
        * [JSdoc example](https://devdocs.io/jsdoc/howto-es2015-modules).
        * At least make sure the students are aware of JSdoc.

### Communicate with the P.O. as often as needed.
You are the focal point between your team and the P.O. Good communication is essential for success of the project.
* Make sure you know which communication medium works best for your team and your client (email, whatsapp, slack...etc).
* Emails are the standard communication method, and should be sent through you only. Your team and the Code Academy staff, including the CF should be included in CC.
* You should discuss the content of the emails with your team before sending/responding. If it's a non-technical matter, and you're not sure what to respond, check with your CF and the CA staff and they will help you.
* Try your best to engage the P.O. on GitHub if they would agree to it. They can see all of your discussions, progress (in term of completed user stories), and leave feedback that is easily understood than through other mediums.
* At least, keep a weekly contact going between your team and the P.O. (if everything is going absolutely smooth, which is rarely the case).
* When things are not clear, ask the P.O.
* If the P.O. is open to it, keep a casual/chat-like channel open with the them. Things like slack or a whatsapp group makes it very easy to talk about small things that can be clarified in a quick response.

### Avoid thinking about any new features during the refactor phase.

---

#### Note: Keep a keen eye on the team: 
Try your best to understand each member's strengths/weaknesses if possible (they shouldn't be limited to technical abilities only). This helps the Code Academy gives targeted feedback and provide effective support for students who are still active after the program has concluded.

# Useful Resources:
* [RESTful design guide](https://medium.com/studioarmix/learn-restful-api-design-ideals-c5ec915a430f)
* [Mavis's Sprint Planning Guide](https://github.com/m4v15/master-reference/blob/master/coursebook/weeks-10-12/build-sprint/preparing-for-build-sprint.md).
* [Documentation Guide](https://hackmd.io/vNeVgzTwSUmK9FJHalczkQ).
* [DWYL contribution guide](https://github.com/dwyl/contributing)
* [DWYL sprint planning guide](https://github.com/dwyl/process-handbook#sprint-planning).
* [Archeticture vs dsign](https://codeburst.io/software-architecture-the-difference-between-architecture-and-design-7936abdd5830)
* [10 common archeticture patterns](https://towardsdatascience.com/10-common-software-architectural-patterns-in-a-nutshell-a0b47a1e9013) (This is more for the Team Lead's own knowledge than to implement in the CA).
