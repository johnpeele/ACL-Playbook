

\[Source\]\(https://playbook.polleverywhere.com/big-picture/code-pipeline/ "Permalink to Code pipeline \| The Poll Everywhere playbook"\)



\# Code pipeline \| The Poll Everywhere playbook



!\[PE Logo White\]\[1\]\[ \]\[2\]



\# \[Code pipeline\]\[3\]



How does Poll Everywhere get code from the fingertips of our engineers into our customers hands at PollEverywhere.com? Through lots of steps that make sure we're shipping a quality product.



\#\# \[Design\]\[4\]



Are you working on something big that's green field? Are multiple people involved in a project? Never underestimate the power of taking some time up front for laying down a design. It can be as simple as sketching out an API in a \[gist\]\[5\] with your pair bear, playing around with what it should look like calling the code in an rspec test, or creating a user-flow diagram to show complex interactions in detail. A little work up front can save tons of work later, especially when people start asking the question, "how is that suppose to work again?"



\#\# \[Planning &amp; pairing up\]\[6\]



During our \[weekly planning meeting\]\[7\], engineers and non-engineers figure out what they're going to build for the week.



To pair or not to pair? That depends on the team sizes and the people involved. There is no "one way" to write code at Poll Everywhere.



\#\# \[Committing code\]\[8\]



Where does all of that code go after it's written? If 20 engineers are working on one project, how do they save all of their files without overwriting each other's work?



Developers don't just save a file and they're done with it, they have to save it somewhere that all other engineers have access to. This central area is called a \[Source Code Repository\]\[9\]. To prevent engineers from clobbering each others work they have to make a "commit" to the repository. Every commit is saved with a comment from a developer describing what they changed, a date and time, the email address of the developer, and a unique fingerprint that represents \_all\_ of the source code in that project at that point in time.



At Poll Everywhere, engineers use a popular source code repository called \[git\]\[10\]. We use \[GitHub\]\[11\] to host our code and follow common \[git conventions\]\[12\].



Git allows engineers to give these fingerprints names. Often you'll hear engineers talking about "branches". Yes, like a tree, engineers can "fork" code from any given point in time, build a new feature in that branch independently of any other developer's branch, then merge it back into the "master" branch when it's all done.



The master branch is a very special branch in all of our projects. It represents the code that is currently in production.



\#\# \[Pull requests\]\[13\]



Some of our work is done through \[pull requests\]\[14\]. It's used by people unfamiliar with a codebase or those who simply want a code review.



However you choose to do it, \_all important code should be looked at by more than one pair of eyes before it's merged to master.\_ Whether through pair programming, pull request, or another type of code review, this will produce better software.



\#\# \[Making sure our code works\]\[15\]



No engineering discipline in the world can ship a product to the world without testing. Software engineers are not immune to this reality so we spend a lot of time thinking about tests.



What is a test? It's as simple as "todo" list to accomplish a task with software. If the product breaks then the test fails. If you get through the list and everything worked ok, the test passed!



Manual tests where humans go through a list of tasks is very useful to catch bugs, but it becomes impractical to have humans do this every time a developer commits code to the source code repository. Like most manual processes through history, computers are up to the task to run automated tests!



You'll hear engineers refer to these tests as unit, integration, or acceptance tests.



\* Unit

\* Integration

\* Acceptance



These tests don't write themselves or somehow magically work. Developers have to write these tests while they are writing the code for the feature they are trying to build.



Automated tests will never replace human testing because it can't catch problems like confusing UI, misspellings, etc, so engineers are expected to manually test features they're building in addition to writing automated tests.



\#\# \[The build broke on CI!\]\[16\]



A code project may end up with thousands of automated tests, but they're not going to do much good unless they're run against the application.



This is where the CI server, or Continuous Integration server, comes into play. Every time a developer makes a commit to a code project, the CI server runs all of the tests against the code to make sure nothing broke. When a developer commits code that inadvertently makes a test fail, we yell, "the build is broken!" and stop working on code until it's fixed. This is similar to the concept of stopping an assembly line in a car factory when a defect is discovered in one of the cars.



\#\# \[Deployment\]\[17\]



When all of the tests pass on the CI server, the code is ready to be deployed to a server so that people can start using it right away.



We're lucky that our Site Reliability team built a handy-dandy CLI tool that lets us provision completely new environments to deploy new features. Were you working on something that you want to show to a customer before deploying to production? Just provision a completely new environment and in less than an hour it will be up and running with a publicly accessible URL. When you're done with it you can destroy the infrastructure with another command.



Don't need a new environment? We maintain several longer-lived staging environments that you can deploy to with a single command.



When everything looks good on staging, a developer can then \[deploy the code to our production environment\]\[18\].



\#\# \[Fixing bugs\]\[19\]



Surprisingly, with all the levels of testing and checking we do to our code, there ends up being bugs that get deployed to production. These bugs are usually reported by customers who are using a combination of software and hardware that our engineers didn't anticipate, or a search engineer crawler hits a URL in a way we didn't anticipate. These unexpected uses result in a web page breaking, which a developer has to fix, test, and deploy.



Big Picture



\[Planning &amp; prioritization\]\[20\]



\[Open source\]\[21\]



\[Code pipeline\]\[22\]



\[Bugs\]\[23\]



\[Architecture\]\[24\]



\[Security\]\[25\]



Day-to-day



\[Working remote\]\[26\]



\[The PollEv Pint™\]\[27\]



\[Weekly cadence\]\[28\]



\[Tools of the trade\]\[29\]



Functions



\[Front end\]\[30\]



\[Apps\]\[31\]



\[Design\]\[32\]



\[Site reliability\]\[33\]



\[Back end\]\[34\]



Appendix



\[Human test suite\]\[35\]



\[30/60/90\]\[36\]



\[Das Pairing Room\]\[37\]



\[Repo admins\]\[38\]



\[Dictionary\]\[39\]



\[Incident response\]\[40\]



\[Conventions\]\[41\]



\#\#\#  \[Big Picture\]\[20\]



\[Planning &amp; prioritization\]\[20\]



\[Open source\]\[21\]



\[Code pipeline\]\[22\]



\[Bugs\]\[23\]



\[Architecture\]\[24\]



\[Security\]\[25\]



\#\#\#  \[Day-to-day\]\[26\]



\[Working remote\]\[26\]



\[The PollEv Pint™\]\[27\]



\[Weekly cadence\]\[28\]



\[Tools of the trade\]\[29\]



\#\#\#  \[Functions\]\[30\]



\[Front end\]\[30\]



\[Apps\]\[31\]



\[Design\]\[32\]



\[Site reliability\]\[33\]



\[Back end\]\[34\]



\#\#\#  \[Appendix\]\[35\]



\[Human test suite\]\[35\]



\[30/60/90\]\[36\]



\[Das Pairing Room\]\[37\]



\[Repo admins\]\[38\]



\[Dictionary\]\[39\]



\[Incident response\]\[40\]



\[Conventions\]\[41\]



\[Edit\]\[42\] \[Blame\]\[43\]



\[1\]: https://playbook.polleverywhere.com/images/pe\_logo\_white.svg

\[2\]: https://playbook.polleverywhere.com/

\[3\]: https://playbook.polleverywhere.com\#code-pipeline

\[4\]: https://playbook.polleverywhere.com\#design

\[5\]: https://gist.github.com/

\[6\]: https://playbook.polleverywhere.com\#planning--pairing-up

\[7\]: https://playbook.polleverywhere.com/big-picture/planning-and-prioritization

\[8\]: https://playbook.polleverywhere.com\#committing-code

\[9\]: https://en.wikipedia.org/wiki/Revision\_control

\[10\]: https://en.wikipedia.org/wiki/Git\_%28software%29

\[11\]: https://github.com/polleverywhere

\[12\]: https://playbook.polleverywhere.com/conventions/git/

\[13\]: https://playbook.polleverywhere.com\#pull-requests

\[14\]: https://help.github.com/articles/using-pull-requests/

\[15\]: https://playbook.polleverywhere.com\#making-sure-our-code-works

\[16\]: https://playbook.polleverywhere.com\#the-build-broke-on-ci

\[17\]: https://playbook.polleverywhere.com\#deployment

\[18\]: https://playbook.polleverywhere.com/big-picture/code-pipeline/deploy-checklist/

\[19\]: https://playbook.polleverywhere.com\#fixing-bugs

\[20\]: https://playbook.polleverywhere.com/big-picture/planning-and-prioritization/

\[21\]: https://playbook.polleverywhere.com/open-source/

\[22\]: https://playbook.polleverywhere.com/big-picture/code-pipeline/

\[23\]: https://playbook.polleverywhere.com/big-picture/bugs/

\[24\]: https://playbook.polleverywhere.com/big-picture/architecture/

\[25\]: https://playbook.polleverywhere.com/big-picture/security/

\[26\]: https://playbook.polleverywhere.com/day-to-day/working-remote/

\[27\]: https://playbook.polleverywhere.com/day-to-day/pint/

\[28\]: https://playbook.polleverywhere.com/day-to-day/weekly-cadence/

\[29\]: https://playbook.polleverywhere.com/day-to-day/tools/

\[30\]: https://playbook.polleverywhere.com/functions/frontend/

\[31\]: https://playbook.polleverywhere.com/functions/native/

\[32\]: https://playbook.polleverywhere.com/functions/design/

\[33\]: https://playbook.polleverywhere.com/functions/sre/

\[34\]: https://playbook.polleverywhere.com/functions/backend/

\[35\]: https://playbook.polleverywhere.com/appendix/human-test-suite/

\[36\]: https://playbook.polleverywhere.com/appendix/30-60-90/

\[37\]: https://playbook.polleverywhere.com/appendix/das-pairing-room/

\[38\]: https://playbook.polleverywhere.com/appendix/repo\_admins/

\[39\]: https://playbook.polleverywhere.com/appendix/dictionary/

\[40\]: https://playbook.polleverywhere.com/appendix/incident-response/

\[41\]: https://playbook.polleverywhere.com/conventions/

\[42\]: https://github.com/polleverywhere/playbook/edit/master/source/big-picture/code-pipeline.html.md

\[43\]: https://github.com/polleverywhere/playbook/blame/master/source/big-picture/code-pipeline.html.md



  

