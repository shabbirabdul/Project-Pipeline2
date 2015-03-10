# DevOps project
 
### Test
#### Run Test Cases, Measure Code Coverage, Publish Reports 

Junit test cases are run after mvn compile. We are using the sonarQube tool to generate code coverage report. Jenkins makes a call to mvn compile which automatically executes all the test cases before measuring the code coverage. 

The Jenkins sonarQube plugin displays the code coverage report on the respective Jenkins Job Page.

#### Improve Testing Coverage

For increasing the test coverage we have used CodePro tool as an Eclipse plugin. CodePro generates test cases for class in the project.

### Analysis
#### Run Static Analysis

We have used sonarQube for static analysis of code. Every detail of the code such as number of functions, lines, directories, files, classes, statements  and accessors are tracked. SonarQube also provides SQALE ranking that tells how well a particular class or a component is written. It also tells what is the complexity /function, /file, /class.

In addition to this, sonar also provides technical issues in the code. It will classify issues in the code to major, minor, critical and blockers. The major ones and the blockers are the ones to be taken care of.

#### Extended analysis

### Reject commit based on testing and analysis result

![alt text] (https://github.ncsu.edu/github-enterprise-assets/0000/2100/0000/0663/f0e0f62c-c6a4-11e4-9e46-5a195d54adc6.png)

