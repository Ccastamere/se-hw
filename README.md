# Git workflow
***
## What is git workflow?
  Workflow is not a primary topic, and the essential problem behind it is actually effective project process management and efficient collaborative development agreement.**Git workflow** is the classic model in the core position, which embodies the experience and essence of workflow. 
***
## Why do we need it?
  * Git workflow makes publishing iteration process smoother by assigning independent branches for function development, publication, preparation and maintenance. 
  * The strict branch model provides some necessary structures for large projects.
  * Git workflow does not use the concepts and commands beyond the functional branch workflow, but assigns a distinct role for different branches, and defines how and when the branches interact with each other.
  * In addition to using functional branches, each branch is defined when preparing, maintaining, and recording publication.
  * You can also use all of the benefits of functional branching workflows: Pull Requests, isolation, experimental development, and more efficient collaboration.
*** 
## How to use it?
### Mode of operation
  Git workflow still uses the central repository as the interactive center for all developers. Like other workflows, developers work locally and push branches into the central repository.
### Historical branches
  Compared with using only one master branch, Git workflow uses two branches to record the history of the project. The master branch stores the history of the formal publication, while the develop branch serves as an integrated branch of functionality. This makes it convenient for all submissions on the master branch to assign a version number. 
![picture]
(https://github.com/xirong/my-git/blob/master/images/git-workflow-release-cycle-1historical.png)
### Functional branches
  Each new function is located in one of its own branches, so that it can be pushed to the central repository to backup and collaborate. But the functional branch does not pull out a new branch from the master branch, but uses the develop branch as the parent branch. When the new function is completed, merge back to the develop branch. New function submission should never interact directly with the master branch. 
### Release branches
  Once the develop branch has enough functionality to make a release (or quickly to a given release date), checkout releases a branch from the develop branch. The new branch is used for release cycle, so the new function can not be added to the branch again - this branch should only do bug repair, document generation and other tasks for release.
### Maintenance branches
  Maintenance branch is used to quickly generate patches for the production releases, which is the only branch that the master branch fork.Once finishing the repair, the modification should immediately merge the master branch and the develop branch, and the master branch should be tagged with the new version number. 
  
