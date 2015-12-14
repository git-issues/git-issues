# git-issues
Issue tracking tool to store issues in your local directory. An addition to git that distributes issue tracking.

## Standard working draft
Git issues is only meant to provide the core functionality, while things such as Github integration are their own
repositories. The following documents the current theory on how to implement this functionality.

1. Storing issues
	* Issues are stored in an xml file that can contain as many superflous tags as needed. It is up to the communication
implementation (Github, JIRA, etc) to deal with only reading the tags they want.
	* Issues are stored in a git submodule to avoid commiting the issues to the repository they belong to as code
	* Multiple issue groups can be stored for one repository and will be maintained in separated named submodules
	* Issue submodules can be committed if there is a desire to use git-issues as your main issue  tracker
2. Accessing issues locally
	* Git issues will provide a method to access the issues in a CLI
