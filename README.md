# WebApp
1) Below mentioned source code and software details.
    JDK1.8
    Eclipse, Junit
    Apache-Tomcat-7.0.75

2) Here, I have build and deployment used DevOps CI/CD.
   Below mentioned Devops tools, what i used for this CI/CD process.

   Jenkins -Build
   Maven   -Compliation
   Stash   -Repository
   Jfrog   -Artifactory
   Git-bash-Access to Repo
   Sonar   -Code Quality
   Ansible -Deployment
   Tomcat  -App Server

3) Below mentioned what kind of job created in jenkins
    1) Build job
    2) Code-Quality job
    3) Deployment job
    4) Testing job
    
   Here i am explaining about each job details.
    1) Build job
         i) Source code management plugin for configuring GIT
        ii) For Build trigger - configured PULL SCM gave schedule H/15****
       iii) Configured – formatted version number ${BUILD_YEAR}${BUILD_MONTH}${BUILDs_THIS_MONTH}
        iv) Artifactory Configured for artifact storing purpose (WAR file maintaining)
         v) For build - gave to maven goals
        vi) Post build action - configured GIT publisher, SMTP email notification and Trigger parameterized build on other projects
       vii) Predefined parameters - build version, project name and environment name

   2)  Code-Quality job
        i) Configured - Execute SonarQube Scanner plugin and mentioned artifact path for download the war file.
       ii) Configured - SMTP email notification and Trigger parameterized build on other projects
       iii) Configured Predefined parameters - build version, project name and environment name

   3) Deployment job
        i) Configured - Invoke Ansible playbook plugin for deplayment purpose and mentioned playbook and inventory path.
       ii) Configured - SMTP email notification and Trigger parameterized build on other projects
      iii) Configured Predefined parameters - build version, project name and environment name

   4) Testing job
        i) Configured - Testcase for validating deployment (Checking the application home page).
       ii) Configured - SMTP email notification  
 
 
     
  Note: For Promating the higher environment purpose - configured promote builds when : Criteria and Action
        I have done poc for build environment dockerized.
 


     






