# Oldenburg - from dwws tutorial

Simple tutorial for a SonarQube testing

1 - Install SonarLint to eclipse
marketplace link : https://marketplace.eclipse.org/content/sonarlint

2 - After installing SonarLint to eclipse, it's already possible to check some failures or bad programming practices on the code
simply go to Project > SonarLint > Analyze.

3 - But we want a more detailed info about the code, such as Reliability, Security, etc. So we need to install the SonarQube server.
it can be download at: https://www.sonarqube.org/downloads/
just click and download the "Community edition".

4 - After downloading it, unzip it and go to /bin folder, inside the unzipped folder.
Inside that bin folder you can find some folders related to all operational systems, just click on the folder for your system.
You've finally found a "sonar.sh" file (if you're on linux or mac).

5 - So, now you are able to run the SonarQube server, simply do it by:
./sonar.sh start

6 - The default link to acces SonarQube server is http://localhost:9000 , if you try to access it, you should see the main page
of the SonarQube server.

7 - Now you will need to login, the default credentials are admin/admin, and then you can go to Projects > Create a new Project
You will have to select the verification method, and then the language of the project and the build of the project.
if the project its in Maven, it will generate a code for you to execute on the project's folder.

8 - After executing the code, and having the building succesfully, you can go to eclipse, 
- Right click on Project > SonarLint > Bind to sonarQube Project
- On "Choose connection type", check "connect to a server"
- Then, provide a URL (in our case http://localhost:9000)
- Choose authentication method
- Choose a name for your connection and click Finish
- Finally, you should write on "Choose the SonarQube Project", the name of the project that you've created on the SonarQube Server.
After that, just click on Finish.

9 - Now if you'd go back to the tab Projects on the SonarQube server, you should see your project linked to eclipse and it's info.
