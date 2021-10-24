Have you ever thought of what a user would do with your application?

No matter how well-architectured the app you built is, _if it brings no value to users, chances are, no one will use it._

In simple terms, **user stories** are brief, informal descriptions of a software feature told from the perspective of the users. These answer the **"who,"** **"what,"** and **"why"** of a single task/functionality in an application.

## User Story Format

```
As a(n) <user type>, I want to <function> so I can <benefit>
```

### Example

As a _customer_, I want to _view the list of menu items_, so I can _easily choose what food to order_.

The **user type** answers the "who," the **function** refers to the "what," and finally, the **benefit** explains the "why" in a user story.

## What Makes a Great User Story?

Now that you know the typical format for a user story, the next question that comes to mind is: _"What makes a great user story?"_. Your backlog should not be filled with stories that actually do not provide user value. If you do, you could waste a lot of time and the effort planning for and working on tasks that don’t add much, if any, business value to your project.

[should have an image]

### INVEST

Fortunately, Bill Wake coined the term "INVEST" which serves as a reminder of what characteristics of a high-quality user story. INVEST stands for:

- **Independent**: User stories should not be dependent on one another.

- **Negotiable**: Should leave space for discussion.

- **Valuable**: Must deliver value to the stakeholders.

- **Estimable**: You should be able to estimate the size and scope of a user story.

- **Small**: The user story should be small enough to easily plan and prioritize it.

- **Testable**: You should be able to test the results of development.

Ideally, your user stories should have all of these characteristics, because they enable you to easily determine how each task fits into your project timeline. By following INVEST, it is much easier to decide which items you must fulfill first, and which ones can wait later.

#### Examples of Bad User Stories

Here are examples of bad user stories, and why they don't work:

> As a customer ordering fast food online, I want to find previous food order lists so that I can see all the orders that I have.

Problem: The benefit/value is absent from this user story, because `so that I can see all the orders that I have` is just a re-statement of `find previous food order lists`.

> As a QA tester, I want to have access to test plans so that when the product is finished, I know how to test it.

Problem: Users do not really care about test plans, they just want quality products.

> As a Jam’s dining customer, I want various food item categories displayed in different colors: red for meats, magenta for grains, and olive green for vegetables and fruits—so that I can easily group my food items by food type.

Problem: The user story is way too technically specific and robotic. This not only fails to represent a user, but also limits the creativity of the developers.

#### Examples of Great User Stories

In contrast to the previous bad examples, here are the user stories that work well:

> As a customer ordering fast food online, I want to find my saved food order lists so that I can reuse them for future orders, allowing me to order faster and more accurately.

> As a Jam’s dining customer, I want items to have a custom item code so that I can quickly find an item on a screen.

> As a logged in user, I would like a login timeout and log off after a certain amount of time so that I can have some protection against unauthorized use when my computer is left unattended

These user stories work well because they have the characteristics of INVEST:

- their functionality is not dependent on other stories
- they leave room for different implementation options
- they add user value to the project
- their scope and size can definitely be estimated by developers
- they are small enough to be planned around and/or reprioritized against other stories
- they can be tested

## Completing a User Story

Now that you know how to make great user stories, you'd probably like to know when they are finished. A user story is completed when it meets its Acceptance Criteria and its Definition of Done (DoD). But what do these terms mean?

### Acceptance Criteria

The Acceptance Criteria of a user story consist of the set of test cases that must be fulfilled to ensure that the software is working as intended. Like user stories should be written from the perspective of a user. They should be clear, concise, and easily utilize by the development team. Acceptance criteria should not be concerned about implementation, but only about which features should be present and included. Each user story will have different Acceptance Criteria based on its requirements.

### Definition of Done (DoD)

The Definition of Done (DoD) is a list of requirements that a user story or Increment must adhere to for the team to call it complete. The DoD serves as a checklist that guides various pre-implementation activities such as discussion, estimation, and design. By ensuring that the DoD is followed, the team can minimize reworking on user stories.

Its difference from Acceptance Criteria is that DoD is common for all the user stories whereas a acceptance criteria is applicable to only a specific user story.

## User Stories in Agile/Scrum Environments

[should have an image]

In Agile/Scrum environments, a team would utilize user stories as part of their Product Backlog. Each story represents a single unit of functionality in a project, and a backlog contains multiple user stories. Unlike a Product Backlog Item (PBI), a user story depicts more than just a specific requirement, change, or bug fix. Its focus is on the end-user and their experience. A user story is an increment that provides value to the overall product. Many teams nowadays use issue trackers or tickets for listing user stories, while others still use sticky notes. As PBIs become higher-ordered in the Product Backlog, they tend to be broken down into user stories with more specific tasks listed.

## Pros and Cons of User Stories

<img src="https://heavencpa.com/wp-content/uploads/2019/03/pros-vs-cons-heaven-and-alvarez-1024x683.png" alt="Pros and Cons" />

### Advantages of User Stories:

- helps ensure that a functionality brings user value
- follows Agile/Scrum core principles
- makes it easier to organize software functionality, as it leaves out implementation details
- allows team members of different expertise and backgrounds to plan an application more easily
- encourages conversations rather than simply handing out document details
- simple to prioritize and reorder, especially for product backlog items
- easily understood by both clients and developers

### Disadvantages of User Stories:

- does not explain the "how?"
- does not involve nonfunctional requirements (e.g. fault tolerance, performance, usability, modifiability)
- user stories are not substitutes to business requirements
- the lack of implementation details means that the processes could vary a lot from team to team
- can be misunderstood and misused
- can lose its original essence/purpose (especially in companies and teams that are "agile" only for compliance purposes)

## Frequently Asked Questions (FAQ)

**Who writes user stories?**

Anyone can write user stories. In a Agile/Scrum environment, the Product Owner is responsible for the backlog of all user stories. However, anyone in the entire team can make them.

**When should you write user stories?**

User stories can be written anytime. Typically, a team will hold a meeting at the start of the project to create user stories to identify initial project requirements. It is impossible to identify all of them at the beginning, so the team will create user stories over the course of the project timeline as they discover more user requirements.

**When is a user story completed or finished?**

A user story is completed when it meets its Acceptance Criteria and its Definition of Done (DoD).

**Do user stories replace a requirements document?**

They don't, as they serve different purposes. A user story focuses on the experience and needs of users, while a requirements document go into a lot of detail about features necessary for a project. User stories focus on the _who_, _what_, and _why_. On the other hand, requirements documents focus on the _what_ and _how_.

**What are the differences between user stories and Product Backlog Items?**

At first glance, they seem similar, but there is a key difference: User stories place an emphasis on the end-users and their experiences. On the other hand, a Product Backlog Item merely represent a specific change, requirement, or bug fix without being concerned much about the _who_.

**Are user stories like pseudocode?**

They are used differently. Pseudocode is mainly concerned about implementation details and how a developer would build a solution, and user stories completely leave out the implementation details in exchange for focusing on the user experience. User stories focus on the _who_, _what_, and _why_. On the other hand, pseudocode focus on the _what_ and _how_.

## Resources/Recommended Reading:

- [User Story Guide by Mike Cohn](https://www.mountaingoatsoftware.com/agile/user-stories#:~:text=User%20stories%20are%20short%2C%20simple,so%20that%20)
- [How To Create a Perfect User Story - Step by Step Guide](https://blog.anvileight.com/posts/how-to-create-a-perfect-user-story-step-by-step-guide/)
- [New to Agile? INVEST in good user stories](https://agileforall.com/new-to-agile-invest-in-good-user-stories/)

### DISCLAIMER:

**This is not a guide**, it is just me sharing my experiences and learnings. This post only expresses my thoughts and opinions (based on my limited knowledge) and is in no way a substitute for actual references. If I ever make a mistake or if you disagree, I would appreciate corrections in the comments!
