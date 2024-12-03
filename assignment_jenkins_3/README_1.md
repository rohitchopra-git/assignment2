# Assignment3

Perform CI checks on  Repositories using Jenkins, store reports, manage artifacts, and set up failure notifications.
API Repositories:
- Java:- https://github.com/opstree/spring3hibernate.git

## Solution

1. Create  a freestyle jobs

![App Screenshot](https://github.com/rohitchopra-git/assignment2/blob/89982913093d7301f24261766fd483667f60cc50/assignment_jenkins_3/New.JPG)

2.Select source code management as git and repository details and credentials

![App Screenshot](https://github.com/OT-MyGurukulam/Jenkins_Batch_28/blob/ce9bd48a5d039411029f495bb20f6b506740f40c/assignment_jenkins_3/G1.JPG)

3. In build step select executive shell and write bash code

![App Screenshot](https://github.com/OT-MyGurukulam/Jenkins_Batch_28/blob/ce9bd48a5d039411029f495bb20f6b506740f40c/assignment_jenkins_3/gbuild1.JPG)

![App Screenshot](https://github.com/OT-MyGurukulam/Jenkins_Batch_28/blob/ce9bd48a5d039411029f495bb20f6b506740f40c/assignment_jenkins_3/gbuild2.JPG)

![App Screenshot](https://github.com/OT-MyGurukulam/Jenkins_Batch_28/blob/ce9bd48a5d039411029f495bb20f6b506740f40c/assignment_jenkins_3/gbuild3.JPG)


   
## Script in Executive Shell

```bash
  
go build -o output_binary_name .
gitleaks detect --exit-code 1 --verbose #credentialScanning
go test -v > result.txt
cat result.txt


```

4. Console output
   
![App Screenshot](https://github.com/rohitchopra-git/assignment2/blob/d45d5d788cd9f31c8ae4094ebff669df49283817/assignment_jenkins_3/gc1.JPG)


5. Git leaks - Credential Scanning
   
![App Screenshot](https://github.com/rohitchopra-git/assignment2/blob/d45d5d788cd9f31c8ae4094ebff669df49283817/assignment_jenkins_3/gc2.JPG)



   
