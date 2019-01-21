# DevOptics Quickstart App

1.  Clone or fork the git repo https://github.com/cloudbees/devoptics-quickstart-app.
2.  Verify maven is installed in Jenkins under "Managing Jenkins" → "Global Tool Configuration".  
3.  Update the "withMaven" argument to match your maven installation from step (2) in the Jenkinsfile.
4.  Create a new multi-branch pipeline called "devoptics-quickstart" in Jenkins, using the repository just created as the source.
5.  Create a new DevOptics application using the JSON in the file application.json, updating the Jenkins URL ("master") if needed.
6.  Make commits, build the master and staging branches, and watch DevOptics work!  Make sure your commits contain JIRA issue ids, like "DEVOPTICS-123".
  
Try making commits that will cause the build to fail, and then adding commits that fix it.

Check out the documentation https://go.cloudbees.com/docs/cloudbees-documentation/devoptics-user-guide/#devoptics-application to extend this example, and adapt to your own, more complex applications.

