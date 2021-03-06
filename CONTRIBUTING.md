## Contributing to react-mobx-router5

Please take a moment to review this document in order to make the contribution process easy and
effective for everyone involved.

Following these guidelines helps to communicate that you respect the time of the developers
managing and developing this open source project. In return, they should reciprocate that respect in
addressing your issue or assessing patches and features.


### Using the issue tracker

The [issue tracker](https://github.com/LeonardoGentile/react-mobx-router5/issues) is the preferred channel
for [bug reports](#bugs), [features requests](#features) and [submitting pull requests](#pull-requests),
but please respect the following restrictions:

* Please **do not** use the issue tracker for personal support requests.
  [Stack Overflow](https://stackoverflow.com/) is a better places to get help.

* Please **do not** derail or troll issues. Keep the discussion on topic and respect the opinions of
  others.


<a name="bugs"></a>
### Bug reports

A bug is a _demonstrable problem_ that is caused by the code in the repository. Good bug reports are
extremely helpful - thank you!

Guidelines for bug reports:

1. **Use the GitHub issue search** &mdash; check if the issue has already been reported.

2. **Check if the issue has been fixed** &mdash; try to reproduce it using the latest `master` or
   development branch in the repository.

3. **Isolate the problem** &mdash; ideally create a reduced test case and a live example.

A good bug report shouldn't leave others needing to chase you up for more information. Please try to
be as detailed as possible in your report. What is your environment? What steps will reproduce the
issue? What browser(s) and OS experience the problem? What would you expect to be the outcome? All
these details will help people to fix any potential bugs.

Example:

> Short and descriptive example bug report title
>
> A summary of the issue and the environment (browser/OS, npm, node, rollup, webpack...with relative versions) in which it occurs. If suitable, include the
> steps required to reproduce the bug.
>
> 1. This is the first step
> 2. This is the second step
> 3. Further steps, etc.
>
> `<url>` - a link to the reduced test case
>
> Any other information you want to share that is relevant to the issue being reported. This might
> include the lines of code that you have identified as causing the bug, and potential solutions
> (and your opinions on their merits).


<a name="features"></a>
## Feature requests

Feature requests are welcome. But take a moment to find out whether your idea fits with the scope
and aims of the project. It's up to *you* to make a strong case to convince the project's developers
of the merits of this feature. Please provide as much detail and context as possible.


<a name="pull-requests"></a>
## Pull requests

Good pull requests - patches, improvements, new features - are a fantastic help. They should remain
focused in scope and avoid containing unrelated commits.

**Please ask first** before embarking on any significant pull request (e.g. implementing features,
refactoring code, porting to a different language), otherwise you risk spending a lot of time
working on something that the project's developers might not want to merge into the project.

Please adhere to the coding conventions used throughout a project (indentation, accurate comments,
etc.) and any other requirements (such as test coverage).

Adhering to the following process is the best way to get your work included in the project:

1. [Fork](https://help.github.com/articles/fork-a-repo/) the project, clone your fork, and configure
   the remotes:

   ```bash
   # Clone your fork of the repo into the current directory
   git clone https://github.com/<your-username>/react-mobx-router5.git
   # Navigate to the newly cloned directory
   cd react-mobx-router5
   # Assign the original repo to a remote called "upstream"
   git remote add upstream https://github.com/LeonardoGentile/react-mobx-router5.git
   # install deps
   npm install
   ```

2. If you cloned a while ago, get the latest changes from upstream:

   ```bash
   git checkout master
   git pull upstream master
   ```

3. Create a new topic branch (off the main project development branch) to contain your feature,
   change, or fix:

   ```bash
   git checkout -b <topic-branch-name>
   ```

4. Test you modification before committing and be sure that your changes don't break previously working code.  
   Everything you need to run the tests should already be installed when you first ran `npm install`. It is also mandatory to lint your code or the automatic build performed by the CI will fail.
 	To run the tests:
 	```
 	npm run test
 	```
 	To run the linter:
 	```
	npm run lint
 	```
 	  
 	Also if you introduce new features or components it is required that you write your unit test for your newly introduced code. Then of course run again `npm run test`. 
 	Before requesting a PR be sure that test and lint did not fail.  

5. Commit your changes in logical chunks. Please adhere to these [git commit message guidelines](https://github.com/angular/angular.js/blob/master/CONTRIBUTING.md#-git-commit-guidelines)
   or your code is unlikely be merged into the main project. 
     
   This repo uses [semantic-release](https://github.com/semantic-release/semantic-release) to automatically 
   bump npm version based on standard commit messages, so it is very important to follow the guidelines.
   To help writing standard commit messages this repo uses [commitizen](http://commitizen.github.io/cz-cli/).  
   In order to make this work please __do not use__ `git commit` for committing your changes but: 
   
   ```bash
   git add .
   npm run commit
   ```
   This will run the npm script `commit` from `packages.json` that will prompt you questions about your 
   changes, please follow the prompted instructions.  
   
   If you don' want to run the npm script you can install _commitizen_ globally with `npm install -g commitizen` 
   and the equivalent command `git cz`. 
   
   Use Git's [interactive rebase](https://help.github.com/articles/about-git-rebase/)
   feature to tidy up your commits before making them public.

6. Locally merge (or rebase) the upstream development branch into your topic branch:

   ```bash
   git pull [--rebase] upstream master
   ```

7. Push your topic branch up to your fork:

   ```bash
   git push origin <topic-branch-name>
   ```

8. [Open a Pull Request](https://help.github.com/articles/using-pull-requests/) with a clear title
   and description.

**IMPORTANT**: By submitting a patch, you agree to allow the project owners to license your work
under the terms of the [MIT License](LICENSE.txt).
