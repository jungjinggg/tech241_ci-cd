# CI/CD
Continuous Integration and Continuous deployment pipelines. It is a method of frequently deliver apps to customers by introducing automation into the stages of app development.

## Why Jenkins?
It is an opensoure automation server which means it's free to use. It provides a wide range of plugins for integration with many test automation tools and frameworks into the test pipeline.

![jenkins](images/jenkins.png)

## CI/CD tools
* GitLab - provides version control, issue tracking and CI/CD capabilities in a signle application.
* Azure DevOps - owned by Microsoft cloud-based platform providing tools for soruce control, build automation, testing and deployment.
* Travis CI - a cloud-based CI/CD platform which intergrates well with Github and offers a simple configuration process. 
* CircleCI - a cloud-based CI/CD platform that offer easy configuration and supports a wide range of programming languages and environments.

## Why buid a pipeline? what are business values?
Benefits of buidling a CI/CD pipeline:
* **Time efficiency** - CI/CD pipelines automate and streamline the software delivery process. This reduces time spent on manual processes and accelerates the time it takes to deliver value to customers.
  
* **Improve quality** - CI/CD pipelines help automated testing, enabling to discover bugs and issue early. By continuously integrating and testing code changes, the business ensures that only quality and reliable software is deployed. Resulting in better customer satisfaction.

* **Increase collaboration and Efficiency** - it encourages collaboration among development, testing and operations teams. This is because it provides an automated workflow, different teams can work together smoothly and continuously. 

* **Continuous improvements** - CI/CD pipelines facilitates a cultire of continuous improvement by providing feedback loops and monitoring performance. This allows the business to discover areas of improvements and can implement changes to enhance software delivery and quality over time.

In summary, CI/CD pipelines allow the business to speed up the software development process significantly. Also, they improve the quality of the software since the code is released in small batch and it is possible to test it thoroughly, allowing to detect and fix bugs before the software is deployed. 

## CI/CD Architecture

![CI/CD pipeline with Jenkins](images/jenkins_diagram.png)


## Implementing CI/CD pipelines
1) Code
2) Build
3) Test
4) Deploy

![ci/cd pipelines](images/CICD_Pipeline.webp)