##### I. Creating the Maven Java Project in Eclipse

1\. Go to File.

2\. Click on New.

3\. Go to Other.

4\. Select the option called Maven project.

5\. Click on Next (ensuring the internet connection is stable).

6\. Click on Next again.

7\. Select an archetype, which serves as the project template.

&nbsp;   ◦ Type org.apache.maven.

&nbsp;   ◦ Wait for the necessary artifacts to display.

&nbsp;   ◦ Ensure the checkbox that says "show the latest version of the archetype" is unchecked.

&nbsp;   ◦ Scroll down and select the Maven archetype quick start. The stable version 1.4 is chosen because it is the easiest way to start a simple Java project.

8\. Click on Next.

9\. Provide a Group ID (this is usually a reverse domain naming structure, like org.apache.maven, used to avoid confusion with similar project names, or a company name like com.app.demo or com.app.kmit).

10\. Provide an Artifact ID, which serves as the project title (e.g., Maven Java project).

11\. Click on Finish.

&nbsp;   ◦ Note: After creation, the project structure includes folders like SRC main Java (for the main code, e.g., app.Java), SRC test Java (for test files), and the vital pom.XML file which manages project settings and dependencies.

II. Manually Running the Maven Build Cycle

Since the objective is to learn how the Maven build tool works manually, the project must be built step-by-step.

1\. Right-click on the project.

2\. Click on Run as.

3\. Select Maven clean.

&nbsp;   ◦ This step deletes the target folder, which contains previous builds of the project.

&nbsp;   ◦ Wait until "build success" appears in the console.

4\. Right-click again and click on Run as.

5\. Select Maven install.

&nbsp;   ◦ This step compiles the Java code and converts it into byte code.

&nbsp;   ◦ Wait until the build is a success.

6\. Right-click again and click on Run as.

7\. Select Maven test.

&nbsp;   ◦ This step tests the project using a default test case, often utilizing JUnit.

&nbsp;   ◦ Wait until build success.

8\. Right-click again and click on Run as.

9\. Select Maven build.

10\. In the resulting prompt, specify the goal.

&nbsp;   ◦ Write clean space install space test.

&nbsp;   ◦ (Alternatively, the goal can simply be written as package, which would also be acceptable).

11\. Click Apply and then Run.

&nbsp;   ◦ Wait until the build is successful, confirming that the .jar file has been generated inside the target folder.

III. Running the Project

1\. Right-click on the project.

2\. Select Run as.

3\. Select Java application.

4\. Click OK.

&nbsp;   ◦ The output (e.g., "hello world") should be displayed in the console.

IV. Pushing the Project to GitHub (Way 1)

1\. Create a new repository in GitHub.

2\. Give the repository a name (e.g., sample Maven Java project).

3\. Scroll down and select the Add .gitignore option.

&nbsp;   ◦ Search for and select the Maven template. Selecting the Maven template ensures that unnecessary files and temporary folders created by Maven (like log files) are not saved to the remote repository.

4\. Click on Create repository.

5\. Go to the Code section and copy the URL of the repository.

6\. Open Git bash in the local system.

7\. In Git bash, type git clone followed by pasting the URL.

8\. Type CD (change directory) and navigate into the newly cloned folder.

9\. In the local file system, navigate to the project directory (e.g., C users > \[your name] > Eclipse Workshop workspace).

10\. Find the project folder that was created (e.g., sample Maven Java project).

11\. Copy all contents from this Eclipse workspace project folder.

12\. Navigate back to the folder that was cloned from GitHub.

13\. Paste everything into this cloned repository folder.

14\. Return to Git bash.

15\. Type git add ..

16\. Type git commit -M followed by a commit message (e.g., sample Maven Java).

17\. Type git push.

18\. Go back to GitHub and refresh the repository page to verify the files have been successfully copied.

Note: The sources state that this is the first method shown for pushing to GitHub; the instructor intends to show another method when creating the Maven web project.





##### I. Creating the Maven Web Project in Eclipse

The initial steps focus on setting up the project using the Eclipse IDE and selecting the appropriate Maven template:

1\. Go to file.

2\. Click on new.

3\. Go to other.

4\. Select the M project.

5\. Click on next.

6\. Click on next again.

7\. Search for the archetype org. Apache.Maven.

8\. Make sure to remove the checkbox.

9\. Scroll down and select the archetype called Maven archetype web app (version 1.4). This archetype is suitable for web applications and includes necessary files like web.xml.

10\. Click on next.

11\. Give a name for the project (e.g., sample Maven web project).

12\. Click on finish.

II. Modifying Project Files

After creation, the presenter modified the default JSP file and prepared to add necessary dependencies via the pom.xml:

1\. Click on the newly created project folder.

2\. Click on SRC main.

3\. Inside main, locate and open the index.jsp file.

4\. Change the data in the file (e.g., to "hello welcome into seab 2024").

5\. Click on save all.

6\. Locate the pom.xml file (which contains configuration details and a default junit testing dependency).

III. Adding the Servlet API Dependency Manually

Since the demonstration focuses on manually working with the Maven build tool, the Servlet API dependency is added by searching online rather than using Eclipse's automatic dependency tool:

1\. Open your browser.

2\. In Google, search for serlet API Maven dependency.

3\. Click on the first Maven repository link that appears.

4\. Scroll down and click on the standard 2.5 version.

5\. Scroll down and copy the dependency tag.

6\. Return to Eclipse.

7\. Paste the dependency tag into the pom.xml file, specifically right before the ending dependency tag.

8\. (Optional but recommended by the video): Remove unnecessary lines, such as the scope.

9\. Click on save all. This step is crucial so the project can talk to the web server.

IV. Building and Running the Project

The project is built using Maven's build life cycle steps and then deployed to a local server:

1\. Right-click on the project.

2\. Go to run as.

3\. Select Maven clean. (Wait for build successful).

4\. Right-click again.

5\. Go to run as.

6\. Select Maven install. (Wait for build success). Note: Install will compile the written code.

7\. Right-click again.

8\. Go to run as.

9\. Go for Maven build.

10\. Under goals, give clean install test.

11\. Click apply.

12\. Click Run. (Wait for build success, indicating the War file has been created in the Target folder since this is a web application).

13\. Right-click on the project.

14\. Select run as.

15\. Select run on server.

16\. Select the deployment server (e.g., Tomcat 9).

17\. Click next and then finish.

18\. Wait for the server to restart and the output to display on the web browser.

V. Pushing the Project to GitHub

The final steps involve initializing a Git repository locally and pushing the content to GitHub:

1\. Create a new repository on GitHub (e.g., sample Maven web project).

2\. Under git ignore, type Maven.

3\. Click create repository.

4\. Go back to Eclipse.

5\. Right-click on the project.

6\. Select show in terminal.

7\. Click on git bash.

8\. In the terminal, execute git init (to initialize the repository).

9\. Execute git add ..

10\. Execute git commit -m "some sample web Maven project" (or desired message).

11\. Execute git remote add origin \[URL], replacing \[URL] with the copied GitHub repository URL, to establish the connection.

12\. Execute git push -U origin master.

13\. Verify that all files are successfully pushed by refreshing the GitHub repository.

The process, from creation to deployment and pushing to GitHub, follows a structured workflow, much like an assembly line where each manual build step—clean, install, test—ensures the quality and completeness of the final product (the War file) before it is shipped (pushed to the cloud).







##### I. Setting Up the Jenkins Build Project (Sample Maven Project Build)

The project functions as a task or job that instructs Jenkins on how to automatically build, test, and deploy code.

1\. Sign In and Create a New Item: Sign in to your Jenkins dashboard and click on "new item".

2\. Name the Project: Give the project a name, such as "Maven sample Maven project build," to indicate its purpose.

3\. Select Project Type: Click on "freestyle project" (which is generally used for basic projects where you can build and test almost anything) and then click "okay".

4\. Configure Source Code Management (SCM):

&nbsp;   ◦ Scroll down to Source Code Management.

&nbsp;   ◦ Click on "git".

&nbsp;   ◦ Paste the URL of the GitHub repository containing the Maven Java project.

&nbsp;   ◦ Specify the branch of the repository where the project resides (e.g., change the default branch to "main").

5\. Define Build Steps (Clean and Install):

&nbsp;   ◦ Go to "build steps" and click "add build step".

&nbsp;   ◦ Select "invoke top 11 Maven targets".

&nbsp;   ◦ Select the Maven version (e.g., Maven\_home), ensuring Maven is properly configured to Jenkins.

&nbsp;   ◦ Set the "goal" to clean (to clean any previous builds).

&nbsp;   ◦ Add a second build step by selecting "invoke top 11 Maven targets" again.

&nbsp;   ◦ Set the "goal" to install.

6\. Define Post Build Actions (Archiving and Triggering Test):

&nbsp;   ◦ Click on "ADD post build action".

&nbsp;   ◦ Select "archive the artifacts" to save the output of the build.

&nbsp;   ◦ Specify the files to archive using \*\*/\*.\* (to save every file and folder obtained as output).

&nbsp;   ◦ Click on "ADD post build action" again.

&nbsp;   ◦ Select "build other projects".

&nbsp;   ◦ Specify the name of the second project (the test project, e.g., "sample Maven project test") to automatically trigger it once the build finishes.

7\. Apply and Save: Click "apply" and then "save".

II. Setting Up the Jenkins Test Project (Sample Maven Project Test)

This project uses the archived output from the build project for testing.

1\. Create New Item for Testing: Return to the dashboard, click on "new item," and name the project (e.g., "sample Maven project test").

2\. Select Project Type: Click on "freestyle project" and "okay".

3\. Prepare Workspace: Scroll down and check the option "delete workspace before build starts" to ensure unnecessary files from the previous project are deleted. (Note: Source code management configuration is not needed here as the build project already provided the repository address).

4\. Copy Artifacts from Build Project:

&nbsp;   ◦ In "add build steps," select "copy artifacts from other project".

&nbsp;   ◦ Specify the source project name (e.g., "Sample Maven project build").

&nbsp;   ◦ Specify artifacts to copy using \*\*/\*.\*.

&nbsp;   ◦ Check the box "stable build only" to ensure testing only triggers if the build was successful.

5\. Define Build Step (Test Goal):

&nbsp;   ◦ Add a build step: Select "invoke top 11 Maven targets".

&nbsp;   ◦ Select the Maven version.

&nbsp;   ◦ Set the "goal" to test.

6\. Archive Test Artifacts:

&nbsp;   ◦ Click on "ADD post build action".

&nbsp;   ◦ Select "archive the artifacts" to save all output files generated during testing.

7\. Apply and Save: Click "apply" and then "save".

III. Creating the Pipeline View

The pipeline provides a graphical representation to combine and visualize the continuous execution of the build and test projects.

1\. Create New Pipeline View: Return to the dashboard and click on the plus symbol (+).

2\. Name the Pipeline: Give the pipeline a name (e.g., "first sample Maven project\_pipeline").

3\. Select View Type: Select "build pipeline View" and click "create".

4\. Specify Initial Project: Scroll down and specify the initial project you want the pipeline to display (e.g., "sample Maven project build").

5\. Apply and Run: Click "apply" and "okay".

6\. Execute the Pipeline: Click "run" in the pipeline view. This will trigger the build project, which automatically triggers the test project, allowing you to see the integrated process graphically





##### building a CI/CD freestyle pipeline using Jenkins for a Maven web project

I. Prerequisites

Before configuring Jenkins, ensure that the Tomcat 9 server is started. The sources specify that credentials for Tomcat (username: admin, password: 1 2 3 4) are found inside the Tomcat-users.XML file located under servers/Tomcat 9 in Eclipse.

II. Creating the Build Project

The first Jenkins project created is for the build phase, named sample Maven web project build.

1\. Create a New Item: Start a new item, give it a name (e.g., sample Maven web project build), and select freestyle.

2\. Add Source Code Management (SCM): Scroll down and add the Git credential. Paste the repository URL and confirm the branch (e.g., Master).

3\. Configure Build Triggers: Select Poll SCM.

&nbsp;   ◦ Schedule a time period using Cron syntax (e.g., five stars \* \* \* \* \* which means the system checks the repository every 1 minute).

4\. Add Build Steps (Maven Targets): Click on add build steps.

&nbsp;   ◦ Invoke top level Maven targets: Set the goal as clean.

&nbsp;   ◦ Invoke top level Maven targets: Set the goal as install.

5\. Configure Post-Build Actions:

&nbsp;   ◦ Archive the artifacts: Specify the artifacts to archive (e.g., star star/ star).

&nbsp;   ◦ Build other project: Specify the next project to trigger (e.g., sample Maven\_test).

6\. Save: Click apply and save.

III. Creating the Test Project

The second project is for the testing phase, named sample Maven web project test.

1\. Create a New Item: Go back to the dashboard, click on new item, paste the name, and select freestyle.

2\. Delete Workspace: Scroll down and configure the project to delete workspace.

3\. Copy Artifacts: Click on copy artifacts from other projects.

&nbsp;   ◦ Copy from the build project (e.g., sample Maven project build).

&nbsp;   ◦ Select stable build only.

&nbsp;   ◦ Specify the artifacts (e.g., star star/ star).

4\. Add Build Steps (Maven Target):

&nbsp;   ◦ Invoke top level Maven targets: Set the goal as test.

5\. Configure Post-Build Actions:

&nbsp;   ◦ Archive the artifacts: Set the path (e.g., star star star/ star).

&nbsp;   ◦ Build other projects: Specify the next project to trigger (e.g., sample Maven web project deploy).

6\. Save: Click apply and save.

IV. Creating the Deploy Project

The third project is for the deployment phase, named sample Maven web project deploy.

1\. Create a New Item: Go back to the dashboard, click on new item, paste the name, and select freestyle.

2\. Delete Workspace: Configure the project to delete workspace before it starts.

3\. Copy Artifacts: Add build step to copy artifacts from other project.

&nbsp;   ◦ Copy from the test project (e.g., sample web project test).

&nbsp;   ◦ Specify the artifacts (e.g., star star/ star).

4\. Configure Post-Build Action (Deployment): Go to add post build action and select deploy war or e to the container.

&nbsp;   ◦ Specify the WAR/EAR files to deploy (e.g., star star/ star.war).

&nbsp;   ◦ Give a context path or name inside which it will be deployed (e.g., sample web project Maven).

&nbsp;   ◦ Add Container: Click on add container and select Tomcat 9.

&nbsp;   ◦ Add Credentials: Add Jenkins credentials using the stored admin and 1 2 3 4 details.

&nbsp;   ◦ Provide the Tomcat URL (e.g., Local Host 80 83).

5\. Save: Click apply and save.

V. Creating the Pipeline View

1\. Create a New View: Go back to the dashboard and click the plus symbol.

2\. Name and Select Type: Give the view a name (e.g., sample web project\_pipeline) and select Build Pipeline.

3\. Configure Initial Job: Select the starting project (e.g., sample Maven web project build).

4\. Complete: Click apply and okay.

Once the pipeline view is created, the process will automatically run: Build, Test, and Deploy will be successfully triggered in sequence. Due to the Poll SCM configuration set in the build job, Jenkins will check the GitHub repository every minute and automatically trigger a new build if changes are found



###### Jenkins scripted pipeline

1\. Creating a New Item: On the Jenkins dashboard, the user clicks on the "new item" option.

2\. Naming and Selecting Pipeline: The user provides a name for the pipeline (e.g., declarative pipeline m in Java) and clicks on the "pipeline" option.

3\. Configuration: After clicking okay, the user scrolls down to the pipeline configuration area and copies and pastes the script into the designated area.

4\. Saving the Configuration: The user clicks apply and then save.

5\. Initial Build: The user initiates the first run by clicking "build now". The system waits for the build to complete, expecting all stages (git repo and clean, install, test, and package) to turn green if successful.

6\. Configuring Automatic Triggering: After a successful build, the user goes back to configure the pipeline.

7\. Selecting Build Triggers: The user navigates to the "build triggers" option. Instead of using Poll SCM (used in a previous experiment, which only triggers if there is a change in the project), the user selects "build periodically".

8\. Setting the Schedule: A schedule is provided, determining how often the project should automatically build, even if there is no change in the code. For example, the user shows that giving five stars (\* \* \* \* \*) will trigger a build every minute.

9\. Saving the Trigger: The user clicks apply and save to enable the automatic triggering.

10\. Observing Automatic Builds: The system then demonstrates that the build automatically triggers based on the set schedule (e.g., after one minute) without the user clicking or modifying the code.

11\. Removing the Trigger: To prevent the unnecessary wasting of the Jenkins server (especially since the 1-minute trigger caused a build failure because the previous build hadn't finished), the user goes back to configure, removes the triggering schedule, clicks apply, and saves the configuration.

12\. Final Manual Build: A final manual build (build now) is executed to confirm a stable and successful run.

13\. Documentation: The final instruction is to take screenshots at every step and save them to a word document.



--------------------------------------------------------------------------------

The process of building and deploying code using Jenkins stages is similar to an assembly line in a factory. The Declarative Script is the blueprint for the entire factory floor. Each Stage (like get repo and clean, install, package) is a dedicated workstation where specific tasks must be completed in order, ensuring quality (testing) and producing the final .jar file (the packaged product). The Build Trigger (like build periodically) acts as an automated timer, ensuring the assembly line starts running at set intervals, whether new orders (code changes) have arrived or not.



Minicube:

---

open windows powershell in ad mode

&nbsp;minikube start

&nbsp;   ◦ This command is the first thing that needs to be typed after opening the Power Shell in administrator mode.

&nbsp;   ◦ It is used to start MiniKube, which creates a local Kubernetes cluster, allowing the management and running of applications on the local system.

2\. kubectl create deployment my-nginx --image=nginx

&nbsp;   ◦ This command is used to create the Nginx application deployment that Kubernetes will manage.

&nbsp;   ◦ kubectl (or cube ctl) is the tool used to talk to Kubernetes.

&nbsp;   ◦ create deployment tells Kubernetes to create an application for managing and running.

&nbsp;   ◦ my-nginx is the name given to the application.

&nbsp;   ◦ --image=nginx specifies the Nginx image (a blueprint) to be used from Docker Hub to create the application. Upon execution, Kubernetes downloads the image, creates a Pod (a container running the application), and automatically starts the Nginx server.

3\. kubectl get deployments

&nbsp;   ◦ This command is used to check or verify that the Nginx deployment (my-nginx) has been created successfully.

&nbsp;   ◦ Note: This command is mentioned as an immediate step after the deployment is created to confirm the application is ready.

4\. kubectl expose deployment my-nginx --type=NodePort --port=80 --target-port=80

&nbsp;   ◦ This command is used to expose the Nginx deployment to the outside world, allowing it to be accessed on a web browser.

&nbsp;   ◦ kubectl expose tells Kubernetes to create a service (a way to expose the application).

&nbsp;   ◦ --type=NodePort makes the service accessible outside the Kubernetes cluster.

&nbsp;   ◦ --port=80 is the port number used to access Nginx from the outside cluster (default for web servers).

&nbsp;   ◦ --target-port=80 is the port inside the Pod/container where Nginx is running.

5\. kubectl scale deployment my-nginx --replicas=4

&nbsp;   ◦ This command is used to scale the application by running more copies (or replicas) to handle more traffic.

&nbsp;   ◦ kubectl scale tells Kubernetes to increase or decrease the number of pods.

&nbsp;   ◦ --replicas=4 specifies that four total copies of the application are desired (three more copies are created since one was already running).

6\. kubectl get deployments

&nbsp;   ◦ This command can be used again to check the deployments and verify that four copies are running after scaling.

7\. kubectl get pods

&nbsp;   ◦ This command can be used to check how many pods are running.

8\. kubectl port-forward svc/my-nginx 8081:80

&nbsp;   ◦ This command is used for port forwarding, allowing the application to be accessed via the web browser.

&nbsp;   ◦ kubectl port-forward forwards traffic from one port to another.

&nbsp;   ◦ svc/my-nginx refers to the my-nginx service.

&nbsp;   ◦ 8081:80 forwards traffic from the local machine's port 8081 (used here because port 8080 was already occupied by Jenkins) to port 80 inside the Nginx container.

9\. minikube dashboard

&nbsp;   ◦ This command is used to open the Kubernetes dashboard, where information about running pods, containers, and deployments can be viewed.

10\. kubectl delete deployment my-nginx

&nbsp;   ◦ This command is the first step in cleaning up the environment, deleting the Nginx application deployment.

11\. kubectl delete service my-nginx

&nbsp;   ◦ This command deletes the service associated with the application.

12\. minikube stop

&nbsp;   ◦ This command is the final step to stop MiniKube and clean up the running environment





Nagios:
 
---

I. Prerequisites and Initial Setup

Before beginning the deployment, certain software and configuration conditions must be met:

Step

Action/Preparation

1\.

Open Docker Desktop and ensure you are signed in.

2\.

Open a suitable terminal, such as PowerShell, in administration mode (or any suitable terminal depending on your operating system).

II. Deploying and Running Nagios

The deployment process involves two primary commands: pulling the necessary image and then running it as a container.

Step

Command

Description

3\.

Pull the Nagios image from Docker Hub.

docker pull jasonrivers/nagios:latest

4\.

Run the Nagios container, name it nagios\_demo, and map the container's internal port 80 to the host's port 80.

docker run --name nagios\_demo -p 80:80 jasonrivers/nagios:latest

III. Accessing the Dashboard and Monitoring

Once the container is launched successfully, Nagios can be accessed via a web browser.

Step

Action/Access Detail

Description

5\.

Access the Nagios Web Interface.

Type localhost:80 into your browser.

6\.

Sign in using the default credentials.

Username: nagiosadmin <br> Password: nagios

IV. Managing Monitoring Features (Host Commands)

After accessing the dashboard, various actions and commands can be performed on the monitored hosts. These are typically available on the right side of the Host Status page under Host Commands.

Step

Action/Command Function

Description

7\.

Locate the host on the map (network map).

See the host location on the network map.

8\.

Stop Nagios from checking the host automatically.

Prevent Nagios from automatically performing checks on the host.

9\.

Forcefully reschedule the next check.

Make Nagios check the host immediately.

10\.

Disable notifications.

Turn off alerts from this specific host.

11\.

Schedule downtime.

Plan a shutdown to avoid unnecessary alerts.

V. Stopping and Removing Nagios

Once finished with the monitoring session, the container and image should be stopped and permanently deleted.

Step

Command

Description

12\.

Verify the running container.

docker ps

13\.

Stop the running container using the container name.

docker stop nagios\_demo

14\.

Remove the stopped container (permanently delete it).

docker rm nagios\_demo

15\.

List all downloaded images to find the exact image name.

docker images

16\.

Remove the Nagios image from the system.

docker rmi <image\_name> (Use the specific image name obtained from step 15)





AWS:
Phase 1: AWS Setup and Launching the EC2 Instance

1\. Start the Lab: Go to the AWS Academy learner site and click on Start Lab.

2\. Access Console: Wait for the radio button to turn green, then click AWS to redirect to the AWS Management Console.

3\. Navigate to EC2: Search for or select EC2 (Elastic Compute Cloud), which is a service providing virtual services (instances).

4\. Launch Instance: Click the EC2 button to reach the dashboard, and then click the Launch Instance option.

5\. Name the Instance: Provide a name for the instance for identification purposes.

6\. Select AMI (OS Image): Select the Application and OS Image (AMI). Choose Ubuntu (a popular, lightweight Linux OS perfect for small applications that provides certain free tier services). Ensure the architecture is selected as 64-bit x86.

7\. Select Instance Type: Select t2.micro. This is part of the free tier and offers 1 CPU and 1GB of RAM.

8\. Create Key Pair Login: Click Create New Key Pair Login. Provide a name (e.g., "my example key pair") and click Create Keypair. This generates a .pem file containing the private key necessary to securely access (log in to) the server via SSH.

9\. Configure Network Settings: In the Network Settings section, make sure to check the boxes for Allow HTTPS traffic and Allow HTTP traffic.

10\. Storage: Keep the default 8GB of free storage.

11\. Launch: Click the Launch Instance option at the bottom right.

12\. Wait for Status Checks: Click on the Instances option and wait for the instance creation to complete. The system is ready when the Instance State is Running and the Status Check shows 2/2 checks passed.

Phase 2: Connecting and Installing Software

1\. Connect to Instance: Select the instance checkbox and click Connect.

2\. Open Terminal: Navigate to the folder where the .pem file was saved and open the Command Prompt or Terminal.

3\. Set Key Permissions: Change the mode/permission of the private key file:

&nbsp;   ◦ Command: chmod 400 <key\_pair\_name>.pem

4\. SSH Login: Copy the SSH command provided in the AWS Connect screen (which includes the private key path and the Ubuntu user/IP address) and paste it into the Terminal.

&nbsp;   ◦ Command (Example Structure): ssh -i <key\_pair\_name>.pem ubuntu@<public\_ip\_address>

5\. Confirm Connection: Type yes when asked for confirmation (Now you are logged into the Ubuntu instance).

6\. Update OS: Update the software packages on the Ubuntu operating system:

&nbsp;   ◦ Command: sudo apt update

7\. Install Docker: Install Docker using the following command:

&nbsp;   ◦ Command: sudo apt --get install docker.io

8\. Install Git: Install Git:

&nbsp;   ◦ Command: sudo apt install git

9\. Install Nano: Install Nano, a text editor for Ubuntu:

&nbsp;   ◦ Command: sudo apt install nano

Phase 3: Application Deployment using Docker

(Note: Prior to this, the source assumes a simple application, like index.html, has been created, committed, and successfully pushed to a remote GitHub repository called, for example, aws\_example\_repo, whose HTTPS path has been copied).

1\. Clone the Repository: Clone the application repository from GitHub onto the EC2 instance:

&nbsp;   ◦ Command: git clone <HTTPS path of repository>

2\. Verify Contents: List the current directory contents:

&nbsp;   ◦ Command: ls

3\. Navigate to Application Folder: Change directory into the cloned application folder (e.g., aws\_example\_repo):

&nbsp;   ◦ Command: cd aws\_example\_repo

4\. Create Dockerfile: Create a Dockerfile using Nano:

&nbsp;   ◦ Command: nano Dockerfile

5\. Populate Dockerfile: Enter the necessary instructions into the Dockerfile (e.g., using Nginx Alpine as the base image and copying application files).

FROM nginx:alpine

COPY . /usr/share/nginx/html

6\. Save and Exit: Use Control+O to save and Control+X to exit Nano.

7\. Build Docker Image: Build the Docker image, giving it a name (e.g., my\_web\_app):

&nbsp;   ◦ Command: sudo docker build -t my\_web\_app .

8\. Run Docker Container: Run the Docker image as a container in detached mode (-d) and map the container port 80 to the host port 80:

&nbsp;   ◦ Command: sudo docker run -d -p 80:80 my\_web\_app

9\. Access Application: Go back to the AWS Instance Dashboard, copy the Public IPv4 address, paste it into a web browser, and press Enter. If the application does not load automatically using HTTPS, switch the protocol to HTTP.

Phase 4: Cleanup and Termination

1\. Check Running Containers: Check which containers are currently running on the server:

&nbsp;   ◦ Command: sudo docker ps

2\. Stop Container: Copy the running container ID and stop it:

&nbsp;   ◦ Command: sudo docker stop <Container ID>

3\. Terminate Instance: To avoid unnecessary costs, go back to the AWS Instance Dashboard, select the running instance, click on Instance State, and choose the option to Terminate or Delete the instance.

4\. End Lab: Wait until the instance state is Terminated, then return to the AWS Academy and click End Lab.

docker:
Skip to content

Chat history





You said:

write a step by step process for:

d)	Write the Docker file and create the image and  access the image in localhost

d)	Create Multi Container of mysql and wordpress through Docker

ChatGPT said:



Thought for 8s

Nice — I’ll give you two clear, copy-pasteable step-by-step recipes:



A simple Dockerfile example (build an image and run it on localhost), and



A multi-container setup that runs WordPress + MySQL using docker-compose.



Each step includes all commands you need. Let’s go.



1\) Write a Dockerfile → build image → access it on localhost

We'll create a tiny static website served by nginx. Folder layout:



project/

├─ app/

│  └─ index.html

└─ Dockerfile

Step A — create content

Create project/app/index.html:



<!doctype html>

<html>

<head><meta charset="utf-8"><title>My Docker Site</title></head>

<body>

&nbsp; <h1>Hello from Docker!</h1>

&nbsp; <p>Served by nginx inside a container.</p>

</body>

</html>

Step B — create Dockerfile

Create project/Dockerfile:



\# Use official nginx base image

FROM nginx:stable-alpine



\# Remove default html and copy our site

RUN rm -rf /usr/share/nginx/html/\*

COPY app/ /usr/share/nginx/html/



\# Expose port (for documentation; docker run -p is what actually publishes)

EXPOSE 80



\# Default nginx command is fine (already in base image)

Step C — build the image

From project/ run:



docker build -t my-static-site:1.0 .

This produces an image called my-static-site:1.0.



Step D — run the container and map to localhost



docker run --name mysite -d -p 8080:80 my-static-site:1.0

-d runs detached.



-p 8080:80 maps container port 80 → host port 8080.



Step E — access it

Open your browser and go to:



http://localhost:8080

You should see “Hello from Docker!”.



Useful commands



See running containers: docker ps



Follow logs: docker logs -f mysite



Stop: docker stop mysite



Remove: docker rm mysite then docker rmi my-static-site:1.0



2\) Create multi-container WordPress + MySQL (recommended: docker-compose)

Use docker-compose to wire WordPress and MySQL together with persistent volumes.



Step A — create a new folder



wp-project/

└─ docker-compose.yml

Step B — docker-compose.yml (copy this)



version: '3.8'



services:

&nbsp; db:

&nbsp;   image: mysql:8.0

&nbsp;   container\_name: wp\_mysql

&nbsp;   restart: unless-stopped

&nbsp;   environment:

&nbsp;     MYSQL\_ROOT\_PASSWORD: rootpassword123    # change for production

&nbsp;     MYSQL\_DATABASE: wordpress

&nbsp;     MYSQL\_USER: wp\_user

&nbsp;     MYSQL\_PASSWORD: wp\_pass\_123

&nbsp;   volumes:

&nbsp;     - db\_data:/var/lib/mysql

&nbsp;   networks:

&nbsp;     - wp-network



&nbsp; wordpress:

&nbsp;   image: wordpress:latest

&nbsp;   container\_name: wp\_app

&nbsp;   depends\_on:

&nbsp;     - db

&nbsp;   restart: unless-stopped

&nbsp;   environment:

&nbsp;     WORDPRESS\_DB\_HOST: db:3306

&nbsp;     WORDPRESS\_DB\_USER: wp\_user

&nbsp;     WORDPRESS\_DB\_PASSWORD: wp\_pass\_123

&nbsp;     WORDPRESS\_DB\_NAME: wordpress

&nbsp;   ports:

&nbsp;     - "8080:80"      # access WordPress at http://localhost:8080

&nbsp;   volumes:

&nbsp;     - wp\_data:/var/www/html

&nbsp;   networks:

&nbsp;     - wp-network



volumes:

&nbsp; db\_data:

&nbsp; wp\_data:



networks:

&nbsp; wp-network:

&nbsp;   driver: bridge

Change MYSQL\_ROOT\_PASSWORD, MYSQL\_USER, and MYSQL\_PASSWORD for any real project.



Step C — start services

From wp-project/ run:



docker compose up -d

or (older Docker Compose):



docker-compose up -d

Step D — wait a moment then access WordPress

Open:



http://localhost:8080

You’ll see the WordPress installation wizard. Create admin user and finish setup.



Step E — common management commands



View logs:



WordPress logs: docker compose logs -f wordpress



MySQL logs: docker compose logs -f db



Stop: docker compose down



To also remove volumes (data), run: docker compose down -v



See containers: docker ps



Inspect network: docker network ls and docker network inspect wp-project\_wp-network (name may vary)



Notes \& best practices



Volumes db\_data and wp\_data keep data persistent across container restarts.



In production, use stronger passwords and consider external database (RDS, Cloud SQL), TLS, backups.



If you want phpMyAdmin, add a phpmyadmin service and link it to db (port mapping e.g. 8081:80).



depends\_on waits for DB container start but does not guarantee MySQL is ready; WordPress retries connections until DB ready.



Quick troubleshooting tips

If WordPress shows database connection error: check DB env vars in compose and run docker compose logs db to confirm MySQL started.



If ports conflict: change 8080:80 to another host port (e.g., 8000:80).



To rebuild after changing Dockerfile or content: docker build again (for single Dockerfile workflow) or docker compose up -d --build for compose.



If you want, I can:



produce a ready ZIP containing these files, or



give you a Dockerfile example for a Node/Java app instead of a static site, or



add a phpmyadmin service to the docker-compose.yml.



Which one should I do next?









No file chosenNo file chosen

ChatGPT can make mistakes. Check important info. See Cookie Preferences.



