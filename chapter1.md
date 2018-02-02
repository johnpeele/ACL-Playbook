# Planning & prioritization

How do we go from an idea to working software that our customers use? There are a lot of moving parts to make sure this happens within the context of a large development team and to maintain the high level of quality our customers expect.

We have a lot to do. New features, bug fixes, UI improvements, code quality, custom client work, internal tools for sales and marketing, metrics, dev work-flow/tools improvements … The list goes on.

We know what to work on and when by prioritizing large team projects (or "Epics") and individual contributions. This starts with an understanding of how our goals align from the individual to the company:

Company Goals → Team Goals → Individual Goals
All goals are completely transparent and shared with the entire team from the company level down to each individual. This means the entire team is involved when setting goals. We avoid goals being prescribed "top down" as this makes for an unhappy team and does not foster product ownership.

Though we make exceptions for critical issues or time sensitive opportunities, we generally try to prioritize on a quarterly basis. This process is cleverly named: Quarterly Planning.

### Quarterly planning

Quarterly planning is informed by our company strategy which is more broadly determined and changes biannually (usually, sometimes it'll be tweaked and discussed at our weekly townhall meeting). The goal of quarterly planning is to prevent too much shifting around and ensure we can deliver larger and more ambitious projects to our customers. These can span from 1 month to 9 months long with shifting team size.

The epic projects are inspired by our strategic goals, but typically come from the ground up. We try to keep quarterly planning as open and transparent as we can without getting stuck in endless meetings. Well before the start of the quarter Product Managers will source and gather ideas from everyone at the company. Then flesh out those which fit with our strategy for more details and discussion.

A set of ideas will then be put up for consideration for the next quarter. Everyone interested in advocating for a given idea/project will then work to put together a short proposal that covers scope of the project, the marketing message, and most importantly…key metrics this project hopes to improve and indicate success. These proposals are combined into a pre-read document that is shared to the whole company and is further fleshed out by any stakeholders and naysayers.

Next, the PMs will organize as few meetings as possible for each idea/project to be presented and discussed in an open meeting for the whole company. These discussion meetings are followed by a smaller meeting to force rank these projects. This will include all of our Functional Advocates in engineering and representatives from each department (sales, marketing, customer support…). And, we are now left with a ranked list of projects we hope to complete!

#### The ranked list of projects

Maintaining a force-ranked list of projects can actually be a lot more difficult than it seems. We always face many distinct challenges, and understanding the tradeoffs is not trivial.

However, the process of ranking these projects pays off for us in several ways.

We think more carefully. The ranking process is a forcing mechanism that requires us to carefully evaluate the cost and value of each project, not just in isolation, but also in relation to each other.

Future planning is more efficient. We are a pretty creative bunch, and we have no end of great ideas to consider during quarterly planning. But it takes a lot of time to evaluate all these ideas. We use the force rank list of projects as a filter mechanism. Before submitting an idea for evaluation, individuals can ask: "Is this new idea more important or valuable than one of the already-ranked projects?" If so, this idea might be a winner. But if not, put the idea on ice for while rather than asking the whole team to evaluate it.

Engineers know where to focus effort. We have a friendly and inclusive work environment, and we prize being considerate of colleagues. But sometimes this leads us to help others at the expense of the projects we are assigned to. The project rank gives engineers a tool to know when putting epic work on hold to help someone is OK. It allows engineers to say, "No," without sacrificing our considerate work environment because everyone involved knows that engineer needs to stay focused on one of the company's top priorities. On the other hand, engineers working on lower-priority epics have the freedom to take on some different work (especially if it supports one of the top ranked projects) without feeling guilty for delaying the assigned epic.

Product Managers have the final decision on the project rank. They are responsible for staying up-to-date with all stakeholders and ensuring the rank is updated when priorities shift.

#### But, how do we know which of these projects we can complete?

I'm glad you asked. The final step in quarterly planning is the actual workplan. This means one last meeting. The PMs and Functional Advocates for the product will meet to discuss how we can best allocate engineering resources(devs and designers). We want to: - Make sure our Bus Factor is low for each project - Try to get engineers who have expressed interest in a project allocated for it - Leave enough wiggle room that we can deal with the unexpected sure to come our way

And, voila! We have a beautiful spreadsheet with all of our hopes, dreams, and priorities for the quarter.

### Priority is never immutable

Priorities are ever changing, and that's OK. We embrace this by ensuring we're prepared to shift our focus quickly. See Being Agile. Just because we spent hours working on a plan does not mean we are stuck to the plan. Sunk cost bias is real.

### Careful, we don't want to become a custom software development shop

It's really easy to have a large customer who wants a specific feature that we don't quite have. We make a conscious effort to make general-purpose solutions.

Product work is prioritized by its effect on the business. We validate these priorities as frequently as possible with our customers so we don't spend a huge amount of time and resources going down the wrong path. One of the most expensive mistakes we can make as a company is building something that people _don't_ want.

MVP, or minimal viable product, is the process of breaking down big ideas and risky assumptions into the smallest possible experiment that we can test. It does _not_ mean that we can ship a sub-par or shoddy product to the customer.

MVP isn't really a product, it's a process of refining the product that spans multiple releases.

Usually we build features that are so big they can't fit within one story, so we build epics with many stories.

Epic teams focus on one feature or product addition comprised of many feature stories. This focus is not always customer facing. Developer assignments are based on the particular needs of the epic. Epic teams consist of a minimum of two developers. The particular developers are assigned based on function (backend, sre, frontend, …)

Epic teams point their own feature stories, hold their own retros, and plan their sprint goals separately with a product manager as needed.

> "Agile software development is a group of software development methods in which requirements and solutions evolve through collaboration between self-organizing, cross-functional teams. It promotes adaptive planning, evolutionary development, early delivery, continuous improvement, and encourages rapid and flexible response to change." 28*

Agile, ASD, CCM, DSDM, Xtreme, FDD, Lean, Kanban, Scrum, Scrum ban … Still with me? No?

**Let's start over:**

* We want to consistently ship value to our customers.

* We want to be able to change directions quickly and easily.

Sprint Planning is the key.

Each epic team sets manageable goals for each sprint. A sprint is a block of time (1 week or 2 weeks). Sprint goals are defined by what the epic team will ship to a user by the end of a single sprint.

Sprint goals are defined in a planning meeting with the epic's developers, designers, and the PM in 30 minute meetings every Tuesday. We: - review whether we hit the previous sprint's goals (and why or why not) - Create a demo for our townhall meeting to show progress and to show off - Determine sprint goals for the next sprint (which starts the following morning after the townhall meeting)

The takeaways for the sprint plan meeting is to retro on the previous sprint's successees/failures, create a demo, and assign pivotal stories to individual team members.

### Defining shipped

It's up to each epic team to define shipped. This definition can vary from team to team. It's essential this definition is set and shared with the company in order to judge the success of a sprint and enforce the creation of achievable sprint goals. If you can't ship _something_ in a sprint, set a different sprint goal.

### Defining the user

Each epic team may have a different user (customers paying via the website, client contracts, internal developers or employees, etc.) Defining the user and what is required to ship to this group also informs sprint goals.

Each epic team manages their own backlog of user stories. User stories encompass the tasks required to achieve a sprint goal. When writing a new pivotal item, make sure to properly classify and label it. Doing so helps us determine how well we are handling our bugs.

User stories are what the team uses to keep track of everything they're working on.

### The actors

There are a few people involved in our work flow:

* **Implementer** - Person that fixes a bug, implements a feature, or completes a chore.

* **Reviewer** - This person validates the bug or feature that an implementer worked on to make sure it meets the requirements stated in the story, is tested, and is fit for a production deploy.

### Stories

Our developers work with user stories from Pivotal Tracker. What's a user story? Let's start with what it's not, and that's a task or chore.

User stories are written in a very specific format so that it describes who the user is, what they want, and why that feature is valuable to them. For example:

> As Thirsty Thomas, I want a beer so that I feel refreshed and get a little silly.

There's a temptation to just write what it is that _you_ want when you start writing user stories. For example:

> Beer

Who wants the beer and why do they want it? There's a little more to writing users stories then that, but you get the idea.

### Points

Points represent the relative complexity of a feature story. "In epic" stories are pointed by the epic team. Stories that don't fit within an epic are pointed with the entire team in our weekly engineering meetings.

| Points | Description |

| ------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |

| 0 | This is a trivial change that you wouldn't write a test for. If you think you want to write a test, then it gets at least 1 point. |

| 1 | You know exactly what to do. There are no unknowns. |

| 2 | You expect it to be pretty easy, but you only have a high-level idea of what is involved. It will take time to work through the complexities. |

| 3 | Significant complexity. Involves several moving parts or something we haven't done before. You might need to investigate or test more than one potential solution. Try breaking this down into smaller stories. |

| 5 | You must put in significant effort to break this into smaller stories. Once or twice per year, if breaking it down is super hard, you can work on a story this complex. |

| 8 | This is just a placeholder story. It must be broken down into smaller stories. |

New features ultimately have bugs, so we don't say it's done until they've all been fixed. After that, the developer can move on to build the next latest and greatest features.

When writing a bug, follow these simple rules to assist in bug maintenance and management over time.

* Can you reproduce your bug? Seriously…have you been able to recreate it 3 times. Then get those repro steps!

* Are there specific preconditions for your bug? If it is browser or OS specific, please add these to pivotal.

* If the bug was reported by a customer, please add a task to notify that customer when it is resolved.

* Include a screenshot or video of the bug if possible. This is always immensely helpful for resolving the issue.

* If the bug is user facing, add a label that matches the bug's GitHub repo name.

* If the bug is discovered during the pre-release development phase, please add a label that matches the epic tracking that feature.

Finishing an epic relies on coordination with other teams (marketing, customer support, sales) within the company. It's up to the product manager and the epic's engineering lead to notify these teams of an epic's progress throughout and ensure each team is able to accomplish their own goals without becoming blocked by the epic team.

Transparency is tantamount for the success of our epic projects. These can be long-term projects with shifting goals, features, and designs. The PM and engineering lead for the project need to disseminate epic progress to the wider company. Typically, this is done through demos during townhall; scheduled HTS's throughout the epic release cycles; and regular (but not overwhelming) reviews from stakeholders of the project for feedback.

An epic does not end when we ship the feature(s) to a user. An epic ends after multiple release cycles. The final sprint of an epic is the cooldown sprint.

### Cooldown sprints

A cooldown sprint allows an epic team to monitor and measure a feature after shipping. This sprint allows the epic team to fix bugs a user may encounter, re-factor code if needed, and wrap up remaining tasks before moving on to a new project or epic team.
