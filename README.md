
![alt text](https://github.com/illwill3314/practice/blob/master/common/images/cerner.png "Logo Title Text 1")

# Openion

Openion is a Web App designed to crowd source opinions and ideas from various associates around Cerner. Its functionality allows for the creation of posts that can have various interactions from commenting to voting.
  - Create Posts 
  - Vote on posts
  - Comment on posts
  - Sort posts based on keywords, votes, comments, and date

Jira: [Go to Jira](https://jira2.cerner.com/browse/ACADEM-54613 "Openion Jira")

### Installation
**Java**
 - This project requires JDK 11: [[Download](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html "Java Download")]
- In your system variables, add JAVA_HOME as the location of your saved Java JDK


![alt text](https://github.com/illwill3314/practice/blob/master/common/images/Enviromental_Variables.PNG)


**Maven**
   - Install Maven 3.1.1: [[Download](https://archive.apache.org/dist/maven/maven-3/ "Maven Download")]
   - In system path variables, add the location of the bin located inside your Maven installation in your local file system (i.e. C:\Users\AB012345\apache-maven-3.1.1-bin\apache-maven-3.1.1\bin )
   - Make sure the following Dependency is added to POM of project when it is installed:
   ```xml
            <plugin>
                <groupId>org.apache.maven.plugins</groupId>
                <artifactId>maven-compiler-plugin</artifactId>
                <configuration>
                    <source>11</source>
                    <target>11</target>
                    <encoding>UTF-8</encoding>
                </configuration>
                <version>3.7.0</version>
            </plugin>
```
   
**Node NPM**
   - Install Node npm [[Download](https://nodejs.org/en/download/ "Node NPM Download")]
   - In system path variables add C:\Users\AB012345\AppData\Roaming\npm 
   
**Clone Openion Project onto Local Machine**
   - Clone the project from Github onto your local machine

**Eclipse IDE**
   - Install the Eclipse IDE: [[Download](https://www.eclipse.org/downloads/ "Eclipse Download")]
   - Import cloned project into Eclipse 
   - You will need to open the Java build path in your project
      - Under libaries click on JRE System Library and ensure JDK 11 is being used
      - Open Java compiler and ensure the compliance level is 11
![alt text](https://github.com/illwill3314/practice/blob/master/common/images/Java_Build_Path.PNG)

**Microsoft Visual Studio** 
   - Install Visual Studio [[Download](https://visualstudio.microsoft.com/vs/ "Visual Studios Download")]
   - Add Workloads: 
     - ASP.net and web development 
     - Azure development 
     - Node.js development
![alt text](https://github.com/illwill3314/practice/blob/master/common/images/Visual_Studio_Workloads.PNG)
 - Add cloned project to space
   
**Logger File**
   - In application properties within the Openion project files, add: 
      -- logging.file = C:\Users\AB012345\Documents\projects\log\openion-logging.log

**PstGreSQL**
   - Install PostgreSQL Database [[Download](https://www.enterprisedb.com/downloads/postgres-postgresql-downloads "PostgreSQL Download")]
   - Ensure that the port number when installing is 5432
   - To open PostgerSQL, search for pgAdmin 4
   - When first opening: 
      - Create Username: postgres
      - Create Password: password
 
### Navigating the Database
- To access tables in database:
   - Expand servers on left side 
   - Expand PostgreSQL 
   - Expand Databases 
   - Expand postgres 
   - Expand Schemas 
   - Expand tables 
   - Right click on table you'd like to view and select view/edit data 
   ![alt text](https://github.com/illwill3314/practice/blob/master/common/images/Database.PNG)
- Initial data is located in resources/db/migration in project files 
- [Database Values](../blob/master/LICENSE)
   
### Running the Application 
- On back end: 
   - In Eclipse, run application.java 
      - Ensure that application starts up in the console 
      ![alt text](https://github.com/illwill3314/practice/blob/master/common/images/Application_Started.PNG)

- On front end: 
   - In Visual Studio, open the developer powershell at the bottom (command line) and navigate to the location of openion-ui in the Openion project
   - Then, type npm start
      - This should open up a new browser window running the application 
![alt text](https://github.com/illwill3314/practice/blob/master/common/images/npm_start.PNG)
- When you would like to restart the application, first make sure you end the program running on Eclipse. 
   - If you do not, you will have to manually close the port the application was using  
   
### Navigating the Application 
   - Landing Page 
      - This page consists of the main feed of posts
      - Posts can be sorted based off of keywords, tags, comment count, and vote count 
         - Using the top search bar will sort the main pages display of posts, based on the entered keyword 
         - Other sort features, including the tags (secondary search bar), comment count, and vote count are located underneath the main search bar 
      - To create a post, users must click on the create post box near the top of the page
         - This will create a popup where the user can give their name, the post description, and any tags relating to the post
      - Each post consists of the posts creator, when the post was created, the content of the post itself, the number of comments, and its total vote score (combined likes/dislikes)
         - Users can vote for a post by clicking the vote button or dislike it by hovering over the same button until other options appear 
         - Clicking on the comment symbol, or in whitespace within the post, will take you to the post specific page where users will be able to interact with one another in the comment section 
         
   - Indiviual Post Page 
      - This page consists of just a single post, and also includes its comments 
      - Users are given the option to remain anonymous or attach their name to a comment 
      - Users also have the opton to like or dislike the post from this page 
