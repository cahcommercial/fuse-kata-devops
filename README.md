  # FUSE DEVOPS AUTOMATION ENGINEERING KATA

* All kata requirements do not need to be coded in order for the kata to be submitted, however requirements implemented 
  should be done so using best practices.
* This is a showcase of skill,not speed.
* When submitting, please let us know what kata requirements were implemented.
* Spend no more than two hours on tha kata.


## [Linux Engineer Instructions]

* The technical exercise for a Fuse Linux DevOps Automation Engineer covers three technologies / concepts that are prevalent in the Fuse environment. In this exercise you will need to create a server in the AWS public cloud (preferably in your personal account), write a simple Chef cookbook, and write a simple Dockerfile. For Chef you will need to write a cookbook that installs an Apache web server listening on port 80, and for Docker you will need to build a containerized NGINX that listens on port 8080 and redirects to port 80 (the Apache web server). The Chef and Docker artifacts need to be deployed to the AWS instance you create, and Fuse will need SSH access to that instance to review the artifacts.

*Amazon Web Services (AWS)
In this section you need to create an Ubuntu AWS EC2 instance where the following sections' artifacts will be deployed to.
1.    Build an amazon node (t2.micro is sufficient) using Ubuntu 14.04 with a public IP address 
2.    Secure it (aside from your local ip or jump box)
a.     Expose ports 22, 80, and 8080 to the following IP: 52.7.76.128
3.    Create a local account which has the ability to login via SSH and sudo to root.  This account will be used to verify the configurations of the host.

## Available Kata's

* [Bowling](http://codingdojo.org/kata/Bowling/) -- [Secondary Link](https://github.com/jonschoning/codingdojo/blob/master/html/kataBowling.html)
* [GameOfLife](http://codingdojo.org/kata/GameOfLife/) -- [Secondary Link](https://github.com/jonschoning/codingdojo/blob/master/html/kataGameOfLife.html)
* [Minesweeper](http://codingdojo.org/kata/Minesweeper/) -- [Secondary Link](https://github.com/jonschoning/codingdojo/blob/master/html/kataMinesweeper.html)
* [PacMan](http://codingdojo.org/kata/PacMan/) -- [Secondary Link](https://github.com/jonschoning/codingdojo/blob/master/html/kataPacMan.html)
* [PokerHands](http://codingdojo.org/kata/PokerHands/) -- [Secondary Link](https://github.com/jonschoning/codingdojo/blob/master/html/kataPokerHands.html)
