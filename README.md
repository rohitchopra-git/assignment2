# Assignment2

Topics Covered:  (User Authentication, User Authorization)

Part 1
There is an organization which has 3 teams based on user roles : 
- Developer
- DevOps
- Testing

  First, you need to create 9 Jenkins jobs. Each job will print its job name, and build number.

    For the Developer, create 3 dummy jobs, visible in the developer view

                job1:- dev-1
                job2:- dev-2
                job3:- dev-3
    For Testing, create 3 dummy jobs, visible in the testing view
  
                job1:- test-1
                job2:- test-2
                job3:- test-3
    For DevOps, create 3 dummy jobs, visible in the devops view
  
                job1:- devops-1
                job2:- devops-2
                job3:- devops-3

Users in each team: 

  developer: [ They can see only dev jobs, can build it, see workspace and configure it ]
               
                - developer-1 
                - developer-2 
  testing: [ They can see all test jobs, can build it, see workspace and can configure it, | They can also view dev jobs ]
                
                - testing-1 
                - testing-2 
  devops:  [ They can see all devops jobs, can build it, see workspace and can configure it, | They can also view dev and test jobs  ]
               
                - devops-1 
                - devops-2
  Administration
                
                -  admin-1 [ It will have full access ]        

See what Authorization strategy suits it and implement it.
Also, go through all authorization strategies.

Legacy mode
Project Based
Matrix Based
Role-Based

Part 2
Enable SSO with Google for admin user


## Solution

1. Create  a freestyle jobs

![App Screenshot](https://github.com/rohitchopra-git/assignment2/blob/662f41a2fa4cf37602a4f3543469a89b90c89195/assignment_jenkins_2/alljob.JPG)

2. Assign roles: manage jenkins > assign role > manage role > global role

![App Screenshot](https://github.com/rohitchopra-git/assignment2/blob/662f41a2fa4cf37602a4f3543469a89b90c89195/assignment_jenkins_2/manage_role_global.JPG)

3. Assign role: manage jenkins > assign role > manage role > item role

![App Screenshot](https://github.com/rohitchopra-git/assignment2/blob/662f41a2fa4cf37602a4f3543469a89b90c89195/assignment_jenkins_2/manage_role_item.JPG)


4. Assign role > global role

![App Screenshot](https://github.com/rohitchopra-git/assignment2/blob/662f41a2fa4cf37602a4f3543469a89b90c89195/assignment_jenkins_2/assign_role_global.JPG)


5. Assign role item > item role
   
![App Screenshot](https://github.com/rohitchopra-git/assignment2/blob/662f41a2fa4cf37602a4f3543469a89b90c89195/assignment_jenkins_2/assign_role_item.JPG)


6. Tester view
![App Screenshot](https://github.com/rohitchopra-git/assignment2/blob/662f41a2fa4cf37602a4f3543469a89b90c89195/assignment_jenkins_2/tester_view.JPG)

7. Devops view

![App Screenshot](https://github.com/rohitchopra-git/assignment2/blob/662f41a2fa4cf37602a4f3543469a89b90c89195/assignment_jenkins_2/devops_view.JPG)

8. Developers view

   ![App Screenshot](https://github.com/rohitchopra-git/assignment2/blob/662f41a2fa4cf37602a4f3543469a89b90c89195/assignment_jenkins_2/devlopers_view.JPG)
