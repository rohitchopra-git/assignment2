# Assignment3

Perform CI checks on  Repositories using Jenkins, store reports, manage artifacts, and set up failure notifications.
API Repositories:
- Java:- https://github.com/opstree/spring3hibernate.git

## Solution

1. Create  a freestyle jobs

![App Screenshot](https://github.com/rohitchopra-git/assignment2/blob/89982913093d7301f24261766fd483667f60cc50/assignment_jenkins_3/New.JPG)

2.Select source code management as git and repository details and credentials

![App Screenshot](https://github.com/rohitchopra-git/assignment2/blob/19b20aaffe3ab3099ccd2fbc45ea242f5ca5b621/assignment_jenkins_3/scm.JPG)

3. In build step select executive shell and write bash code

![App Screenshot](https://github.com/rohitchopra-git/assignment2/blob/d45d5d788cd9f31c8ae4094ebff669df49283817/assignment_jenkins_3/Build.JPG)

   
## Script in Executive Shell

```bash
  
mvn checkstyle:checkstyle   #codeQuality
mvn clean test              #unitTest
mvn cobertura:cobertura     #code Coverage
gitleaks detect --source=$WORKSPACE --report-path=$WORKSPACE/gitleaks-report.json #credentialScanning

```


4. Dependency Check

![App Screenshot](https://github.com/rohitchopra-git/assignment2/blob/d45d5d788cd9f31c8ae4094ebff669df49283817/assignment_jenkins_3/DependencyJPG.JPG)

 
5. Result of checkstyle

![App Screenshot](https://github.com/rohitchopra-git/assignment2/blob/d45d5d788cd9f31c8ae4094ebff669df49283817/assignment_jenkins_3/checkstyle.JPG)


6. Result of clean test

![App Screenshot](https://github.com/rohitchopra-git/assignment2/blob/d45d5d788cd9f31c8ae4094ebff669df49283817/assignment_jenkins_3/clean.JPG)


![App Screenshot](https://github.com/rohitchopra-git/assignment2/blob/d45d5d788cd9f31c8ae4094ebff669df49283817/assignment_jenkins_3/clean1.JPG)

7. Cobertura code coverage report

![App Screenshot](https://github.com/rohitchopra-git/assignment2/blob/d45d5d788cd9f31c8ae4094ebff669df49283817/assignment_jenkins_3/cobertura.JPG)


![App Screenshot](https://github.com/rohitchopra-git/assignment2/blob/d45d5d788cd9f31c8ae4094ebff669df49283817/assignment_jenkins_3/cobertura1.JPG)

8. Git leaks - Credential Scanning
   
![App Screenshot](https://github.com/rohitchopra-git/assignment2/blob/d45d5d788cd9f31c8ae4094ebff669df49283817/assignment_jenkins_3/gitleaks.JPG)

9. Dependency Check

![App Screenshot](https://github.com/rohitchopra-git/assignment2/blob/fe01e5af0a8786e8299ffa805e655ddebf0aa0c8/assignment_jenkins_3/Dependency1.JPG)

![App Screenshot](https://github.com/rohitchopra-git/assignment2/blob/fe01e5af0a8786e8299ffa805e655ddebf0aa0c8/assignment_jenkins_3/Dependency2.JPG)


   
