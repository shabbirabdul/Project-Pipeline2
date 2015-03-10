# DevOps project
 
### Test
#### Run Test Cases, Measure Code Coverage, Publish Reports 

Junit test cases are run after mvn compile. We are using the sonarQube tool to generate code coverage report. Jenkins makes a call to mvn compile which automatically executes all the test cases before measuring the code coverage. 

The Jenkins sonarQube plugin displays the code coverage report on the respective Jenkins Job Page.

#### Improve Testing Coverage

For increasing the test coverage we have used CodePro tool as an Eclipse plugin. CodePro generates test cases for class in the project.

![alt text] (https://github.ncsu.edu/github-enterprise-assets/0000/2100/0000/0667/23c959be-c6bc-11e4-9cb9-efc849e4f356.png)

Report after improvement:

![alt text] (https://github.ncsu.edu/github-enterprise-assets/0000/2100/0000/0669/ad4711d0-c6bd-11e4-8d74-ceeb9cc66126.png)

### Analysis
#### Run Static Analysis

We have used sonarQube for static analysis of code. Every detail of the code such as number of functions, lines, directories, files, classes, statements  and accessors are tracked. SonarQube also provides SQALE ranking that tells how well a particular class or a component is written. It also tells what is the complexity /function, /file, /class.

In addition to this, sonar also provides technical issues in the code. It will classify issues in the code to major, minor, critical and blockers. The major ones and the blockers are the ones to be taken care of.

#### Extended analysis

![alt text] (https://github.ncsu.edu/github-enterprise-assets/0000/2100/0000/0665/f1f90d50-c6af-11e4-9320-9cab305c9a12.png)

### Reject commit based on testing and analysis result

![alt text] (https://github.ncsu.edu/github-enterprise-assets/0000/2100/0000/0668/2685b526-c6bc-11e4-85be-8b2b2bf2bbc0.png)

![alt text] (https://github.ncsu.edu/github-enterprise-assets/0000/2100/0000/0663/f0e0f62c-c6a4-11e4-9e46-5a195d54adc6.png)

