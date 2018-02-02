# Code pipeline

How does Poll Everywhere get code from the fingertips of our engineers into our customers hands at PollEverywhere.com? Through lots of steps that make sure we're shipping a quality product.

## Design

Are you working on something big that's green field? Are multiple people involved in a project? Never underestimate the power of taking some time up front for laying down a design. It can be as simple as sketching out an API in a gist with your pair bear, playing around with what it should look like calling the code in an rspec test, or creating a user-flow diagram to show complex interactions in detail. A little work up front can save tons of work later, especially when people start asking the question, "how is that suppose to work again?"

## Planning & pairing up

During our weekly planning meeting, engineers and non-engineers figure out what they're going to build for the week.

To pair or not to pair? That depends on the team sizes and the people involved. There is no "one way" to write code at Poll Everywhere.

## Committing code

Where does all of that code go after it's written? If 20 engineers are working on one project, how do they save all of their files without overwriting each other's work?

Developers don't just save a file and they're done with it, they have to save it somewhere that all other engineers have access to. This central area is called a Source Code Repository. To prevent engineers from clobbering each others work they have to make a "commit" to the repository. Every commit is saved with a comment from a developer describing what they changed, a date and time, the email address of the developer, and a unique fingerprint that represents _all_ of the source code in that project at that point in time.

At Poll Everywhere, engineers use a popular source code repository called git. We use GitHub to host our code and follow common git conventions.

Git allows engineers to give these fingerprints names. Often you'll hear engineers talking about "branches". Yes, like a tree, engineers can "fork" code from any given point in time, build a new feature in that branch independently of any other developer's branch, then merge it back into the "master" branch when it's all done.

The master branch is a very special branch in all of our projects. It represents the code that is currently in production.

## Pull requests

Some of our work is done through pull requests. It's used by people unfamiliar with a codebase or those who simply want a code review.

However you choose to do it, _all important code should be looked at by more than one pair of eyes before it's merged to master._ Whether through pair programming, pull request, or another type of code review, this will produce better software.

## Making sure our code works

No engineering discipline in the world can ship a product to the world without testing. Software engineers are not immune to this reality so we spend a lot of time thinking about tests.

What is a test? It's as simple as "todo" list to accomplish a task with software. If the product breaks then the test fails. If you get through the list and everything worked ok, the test passed!

Manual tests where humans go through a list of tasks is very useful to catch bugs, but it becomes impractical to have humans do this every time a developer commits code to the source code repository. Like most manual processes through history, computers are up to the task to run automated tests!

You'll hear engineers refer to these tests as unit, integration, or acceptance tests.

* Unit
* Integration
* Acceptance

These tests don't write themselves or somehow magically work. Developers have to write these tests while they are writing the code for the feature they are trying to build.

Automated tests will never replace human testing because it can't catch problems like confusing UI, misspellings, etc, so engineers are expected to manually test features they're building in addition to writing automated tests.

## The build broke on CI!

A code project may end up with thousands of automated tests, but they're not going to do much good unless they're run against the application.

This is where the CI server, or Continuous Integration server, comes into play. Every time a developer makes a commit to a code project, the CI server runs all of the tests against the code to make sure nothing broke. When a developer commits code that inadvertently makes a test fail, we yell, "the build is broken!" and stop working on code until it's fixed. This is similar to the concept of stopping an assembly line in a car factory when a defect is discovered in one of the cars.

## Deployment

When all of the tests pass on the CI server, the code is ready to be deployed to a server so that people can start using it right away.

We're lucky that our Site Reliability team built a handy-dandy CLI tool that lets us provision completely new environments to deploy new features. Were you working on something that you want to show to a customer before deploying to production? Just provision a completely new environment and in less than an hour it will be up and running with a publicly accessible URL. When you're done with it you can destroy the infrastructure with another command.

Don't need a new environment? We maintain several longer-lived staging environments that you can deploy to with a single command.

When everything looks good on staging, a developer can then deploy the code to our production environment.

## Fixing bugs

Surprisingly, with all the levels of testing and checking we do to our code, there ends up being bugs that get deployed to production. These bugs are usually reported by customers who are using a combination of software and hardware that our engineers didn't anticipate, or a search engineer crawler hits a URL in a way we didn't anticipate. These unexpected uses result in a web page breaking, which a developer has to fix, test and deploy.

