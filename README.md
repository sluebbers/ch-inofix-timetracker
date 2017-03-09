# ch-inofix-timetracker
A timetracker plugin for Liferay.

## How To Build
1. Install blade: `curl https://raw.githubusercontent.com/liferay/liferay-blade-cli/master/installers/local | sh`
1. Create a liferay workspace: `blade init [WORKSPACE_NAME]`
1. Checkout timetracker sources to the workspace's module directory: `cd [WORKSPACE_NAME]/modules; git clone https://github.com/inofix/ch-inofix-timetracker.git`
1. Run ServiceBuilder: `gradle buildService`
1. Build: `gradle jar`

## How To Contribute
1. Fork this repository to your individual github account.
1. Clone your personal fork to your local machine.
1. Use feature branches to work on new features or known issues.
1. Merge finished features into your individual master branch and 
1. create pull-requests, to contribute your solutions to the inofix master branch.
1. Stay up-to-date:
1. Change the current working directory to your local project.
1. Configure https://github.com/inofix/ch-inofix-timetracker as additional upstream remote (see: https://help.github.com/articles/configuring-a-remote-for-a-fork/)
1. Sync inofix-master with your individual fork (see: https://help.github.com/articles/syncing-a-fork/): 
1. Fetch upstream/master to your local copy: 'git fetch upstream' 
1. Check out your fork's local 'master' branch: 'git checkout master'
1. Merge the changes from 'upstream/master' into your local master branch. This brings your fork's master branch into sync with the upstream repository, without losing your local changes: 'git merge upstream/master'
1. Push merged master to your individual github account and 
1. create a pull-request, to contribute your solution to the inofix master branch.

Note for Eclipse / Liferay-IDE developers: if the JSPs of the timetracker-web project aren't validated properly, 
- select the timetracker-web in the Project-Explorer view
- open the context menu with the right mouse key
- select "Configure" and
- choose "Add JSP Validation Support"
- select the timetracker-web in the Project-Explorer view
- choose CTRL + F5 to refresh your project
You may have to restart Eclipse, too in order to have your JSPs validated.

## How To Test

Make sure, you have created the autogenerated service- and model-classes (see above).

1. Setup tomcat-bundle for testing: `cd [WORKSPACE_NAME]; gradle initBundle`
1. Change to project directory: `cd ch-inofix-timetracker`
1. Run check task: `gradle check`
1. Review integration test results: `firefox timetracker-test/build/reports/tests/index.html`

Latest Travis-test-results for ch-inofix-timetracker can be found at https://travis-ci.org/inofix/ch-inofix-timetracker/builds
