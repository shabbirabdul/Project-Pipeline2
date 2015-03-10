# DevOps Milestone 2: Test and Analysis
 
### Test
#### Task 1: Run Test Cases, Measure Code Coverage, Publish Reports 

Junits are run by executing Maven compile and install tasks. We are using the Jacoco tool to generate code coverage report. Jacoco integrates with SonarQube to display coverage details. Jenkins makes a call to mvn compile which automatically executes all the test cases before measuring the code coverage. The Jenkins sonarQube plugin displays the code coverage report on the respective Jenkins Job Page.

![alt text] (https://github.ncsu.edu/github-enterprise-assets/0000/2100/0000/0664/f5eed594-c6a4-11e4-8e0a-45066c503894.png)

#### Task 2: Improve Testing Coverage

For increasing the test coverage we have used CodePro tool as an Eclipse plugin. CodePro generates test cases for every class in the project. The project under test is a small sample maven project created to measure code coverage metrics for this project. 
Github link of the project: https://github.com/shabbirabdul/LilyPadCompass

Test coverage before improvement:

Few Java classes were added to the project and test coverage is measured.

![alt text] (https://github.ncsu.edu/github-enterprise-assets/0000/2100/0000/0667/23c959be-c6bc-11e4-9cb9-efc849e4f356.png)

Test coverage after improvement:

CodePro is a random test case generating tool, which when used with a project will generate test cases for every class in the project. The test classes generated have names ending with Test and all the test cases generated are available under src/test/java under the same project.

![alt text] (https://github.ncsu.edu/github-enterprise-assets/0000/2100/0000/0669/ad4711d0-c6bd-11e4-8d74-ceeb9cc66126.png)

We also used Cobertura for code coverage. The screenshot explains various aspects of code coverage captured by Cobertura.

![alt text] (https://github.ncsu.edu/github-enterprise-assets/0000/2100/0000/0673/9f5f5a14-c6c2-11e4-84a0-4eb5ad488c91.png)

### Analysis
#### Task 3: Run Static Analysis

We have used sonarQube for static analysis of code. Every detail of the code such as number of functions, lines, directories, files, classes, statements  and accessors are tracked. SonarQube also provides SQALE ranking that tells how well a particular class or a component is written. It also tells what is the complexity /function, /file, /class. In addition to this, sonar also provides technical issues in the code. It will classify issues in the code to major, minor, critical and blockers. The major ones and the blockers are the ones to be taken care of.

Sonar identifies problematic parts of the code, classifies them into minor, critical, major etc. Giving an idea for the developer to prioritize solving bugs in the code. 

![alt text] (https://github.ncsu.edu/github-enterprise-assets/0000/2100/0000/0670/fb0cdb76-c6c1-11e4-8f3c-ec7d61cd89d0.png)


![alt text] (https://github.ncsu.edu/github-enterprise-assets/0000/2100/0000/0671/fe2183a2-c6c1-11e4-962f-ad661b00c8dd.png)

![alt text] (https://github.ncsu.edu/github-enterprise-assets/0000/2100/0000/0672/00f256b0-c6c2-11e4-84e2-796c39e354bc.png)


#### Task 4: Extended analysis

We have developed a static analysis tool that generates the number of lines of comments, code and ratio of comments to code. We have integrated it with Jenkins build, during the build this plugin is run with the path to source code as an argument. The jar file scrapes through all Java files and counts number of comments and lines in the code. The following screen shot shows comment ratio captured during jenkins build.
Github link for Comments Analyzer Tool: https://github.com/shabbirabdul/CommentsAnalyzer

![alt text] (https://github.ncsu.edu/github-enterprise-assets/0000/2100/0000/0665/f1f90d50-c6af-11e4-9320-9cab305c9a12.png)

### Task 5: Reject commit based on testing and analysis result

Cobertura Gate

The Cobertura Jenkins Plugin allows us to reject a build if the code coverage falls beyond the mentioned threshold. The screenshot below describes the cobertura threshold used in this project that causes the build to fail due to low coverage.

![alt text] (https://github.ncsu.edu/github-enterprise-assets/0000/2100/0000/0668/2685b526-c6bc-11e4-85be-8b2b2bf2bbc0.png)

![alt text] (https://github.ncsu.edu/github-enterprise-assets/0000/2100/0000/0663/f0e0f62c-c6a4-11e4-9e46-5a195d54adc6.png)

