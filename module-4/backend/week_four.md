## Week Four - Module 4 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week. 

Note: When you're done, submit a PR. 

* What's the purpose of a project management tool?
Project management tools allow us to produce a detailed plan of how to approach each sprint of the project, give us the ability to estimate the points required to complete each task and keep us on task by making & ordering discrete issue cards to accomplish.

* What's your favorite project management tool?
Each one I've used and seen has its own advantages; I love waffle for allowing you to add labels of any color, showing the label title on the abbreviated cards, and allowing you to customize and add columns. It is also easily integrated into GitHub. Pivotal Tracker only has one color for labels & doesn't allow you to customize columns, but allows you to easily assign points to tasks & keep track of completed points. It also allows you to easily identify whether a task is a feature, bug or chore, and provides flags assigned to dates to help you keep on track for whatever chunk of time you define.

* Why do we create staging environments?
Staging environments are important for offering a means for a non-technical person to view and interact with your application as it would look and feel in production. This helps to get input for fine-tuning details and ensuring functionality is satisfactory before going live.

* What are the characteristics of a good README (in your opinion)?
Explanation/motivation for the project
List of contributors
Relevant links
Instructions for setup and testing
Clear, concise steps with code blocks
Screenshots & screencasts

* What's one main improvement you're going to make to your code regarding accessibility issues?
Improve tabbing with tabindex!

* What are some basic security concerns to be aware of when building applications?
Injection (inserting instructions where only data is intended)
Click Hijacking (overlay original site in an iframe)
Replay (resending requests)
Man in the middle (something listening to traffic between a client and server, and inserting data)

* Why is continuous integration helpful/important?
Continuous integration provides a means of pushing to production automatically after a predetermined set of requirements is met/steps are taken. Generally, a complete testing of the application is conducted automatically in conjunction with the CI tool, so in addition to saving the developer time and energy to manually push to production, it offers a thorough check that the app is bug-free (according to your tests at least).

* What are some continuous integration tools?
Travis CI


#### Review  

* What are some characteristics of "good" git workflow?
Solid git workflow includes checking out a branch for every task card, committing often, rebasing commits on completion, running tests before pushing to a remote repo, creating pull requests for completed features & fixes or for a work-in-progress that you would like feedback on, providing feedback on others' PRs, and merging PRs into master after thorough review is completed.

* What are the four fundamental concepts of object oriented programming?
Inheritance (classes can inherit methods or functions from other classes and modules), polymorphism (inherited methods and functions can be redesigned within the sub-class), abstraction (excluding certain properties from anything/anybody that doesn't need to know about it, and encapsulation (segmenting portions of functionality into "capsules"; helps to keep things singularly-responsible and augments abstraction/privacy).

* What's a module in Ruby and what's the difference between a class and a module?
A module is an encapsulating object that can be inherited into classes or wrap classes into families. It cannot be instantiated (doesn't change state) like a class.
