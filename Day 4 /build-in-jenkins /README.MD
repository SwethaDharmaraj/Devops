Summary:
This Project demonstrates basic CI automation.
This workflow helps understand automated build execution and continuous integration basics.
Login Jenkins

(Authentication required)

Create a new CI/CD Workflow:

Select Add Item from side panel
Each item = one automated process
Add new item > Item Name > Free Style Project

Create Item

Configure Automation steps

Inside Item’s Configure > Build Steps > Execute Shell > Type the below

echo "sample run" > HelloWorld.txt
The above command prints text and redirects output to HelloWorld.txt (created)

Now Apply & Save

Now in Side Panel > Build Now

Now, Jenkins allocates workspace
Runs shell script
Executes command
Generate Output
Check Console Output inside Builds

Jenkins holds logs of every step
Shows command execution details
See your Build Status

Jenkins marks build:
SUCCESS → if script runs properly
FAILURE → if error occurs
![jenkins-console-output.png]

Note the line workspace: copy /var/lib/jenkins/workspace/HelloWorld

Check below image

![local-vm-output.png]
