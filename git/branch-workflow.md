# Git: Commands of a pull request
## [Saving changes](https://www.atlassian.com/git/tutorials/saving-changes)
### git add
* Tell Git you want to include updates to a particular file in the next commit.
* Needs to be called every time you alter a file.

### The staging area
* Think of it as a buffer between the working directory and project history.
* Instead of committing all of the changes you've made since the last commit, the stage lets you
  group related changes into highly focused snapshots before actually commititing it to to the
  project history.
* However, it's important to create atomic commits so that it’s easy to track down bugs and revert
  changes with minimal impact on the rest of the project.

### git commit
* Commits the staged snapshot to the project history.
* Git will never change them unless you explicity ask it to.
* Only happens in local repository.
* Think of the local repository as a buffer between their contributions and the central repository.
    * Split new feature into atomic commits and then push entire feature to central repository.
    * Lets developers work in an isolated environment, deferring integration until they’re at a
      convenient break point.

## [Using branches](https://www.atlassian.com/git/tutorials/using-branches)
### git branch
* A branch represents an independent line of development.
* You can think of them as a way to request a brand new working directory, staging area, and
  project history.
* The command lets you create, list, rename, and delete branches.
    * Once you’ve finished working on a branch and have merged it into the main code base, you’re
      free to delete the branch without losing any history.
    * If the branch has not been merged you'll have to force delete the branch.

### git checkout
* Lets you navigate between the branches created by git branch.

### git merge
* Lets you take the independent lines of development created by git branch and integrate them into
  a single branch.
* Merges into current branch. The current branch will be updated to reflect the merge, but the
  target branch will be completely unaffected.

## [Making a pull request](https://www.atlassian.com/git/tutorials/making-a-pull-request/)
### Feature branch workflow
* Uses a shared Bitbucket repository for managing collaboration
* Developers create features in isolated branches
* Developers should open a pull request to initiate a discussion around the feature before it gets
  integrated into the main codebase.

### Using SourceTree to make a pull request using the feature branch workflow
* Select repository
* Pull to get latest
* Create new branch named after your feature
* Implement new feature
    * Make changes
    * Stage
    * Add comment
    * Commit
    * Repeat until feature is implemented
* Right-click on branch and select Create pull request...
* On Bitbucket.org verify your feature is being merged into master
* Add reviewers
* Update description
* Check Close branch
* Click create pull request
