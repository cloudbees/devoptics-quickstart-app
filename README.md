# DevOptics Quickstart

1.  Clone or fork the git repo https://github.com/cloudbees/devoptics-quickstart-app.
2.  Create a new multi-branch pipeline called "devoptics-quickstart" in Jenkins, using the repository just created as the source.
3.  Create a new DevOptics application using the JSON in the file application.json, updating the Jenkins URL ("master") if needed.
4.  Make commits, build the master and qa branches, and watch DevOptics work!  Make sure your commits contain JIRA issue ids, like "DEVOPTICS-123".  
5.  Try making commits that will cause the build to fail, and then adding commits that fix it.