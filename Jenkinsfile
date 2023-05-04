pipeline{  
    agent any
    stages{
        stage('Build'){
            steps{
                echo "Tool Used: Maven"
                echo "Maven is a tool that automates the process of building Java software. We use a project object model (POM) to define our project's structure and dependencies, and Maven uses plugins to run tasks like compiling code, running tests, and packaging our program. This saves us time and ensures consistency across different projects."
            }
        }
        stage('Unit and Integration Tests'){
            steps{
                echo "Tool Used: Emma"
                echo "Emma is a tool used for Unit and Integration testing in Java programming. It helps ensure that code works correctly and doesn't have bugs by tracking how much of it is being tested. It helps ensure that tests are thorough and that we're testing as much of our code as possible, which can help catch bugs earlier and reduce the time spent debugging. Emma is widely used in the Java community, making it a reliable tool for testing across different projects."
            }
            post{
                success{
                    mail to: "arshsure@gmail.com",
                    subject: "Build Status Email",
                    body: "Unit and Integration Tests was a success"
                }
            }
        }
        stage('Code Analysis'){
            steps{
                echo "Tool Used: Checkstyle"
                echo "Checkstyle is a tool used for Code Analysis in Java programming. It helps us ensure that our code is readable, maintainable, and follows coding standards by checking it against a set of predefined rules and guidelines. It also helps us catch potential issues early and improve the readability and maintainability of our code. It is widely used in the Java community, ensuring that our coding standards are consistent and reliable across different projects."
            }
        }
        stage('Security Scan'){
            steps{
                echo "Tool Used: Probley"
                echo "Probley is a tool used for Security Scans in web applications. It helps ensure that web applications are secure and free from vulnerabilities that can be exploited by attackers by scanning their code and detecting any potential security issues. It also helps catch potential security issues early and reduce the risk of a security breach. Probley is widely used in the web development community, ensuring that the security scanning process is consistent and reliable."
            }
            post{
                success{
                    mail to: "arshsure@gmail.com",
                    subject: "Security Scan Status Email",
                    body: "Security Scan was a success"
                }
            }
        }
        stage('Deploy to Staging'){
            steps{
                echo "Tool Used: AWS EC2"
                echo "Staging environments are used to test our applications in an environment similar to production, but where changes can be made without affecting actual users. AWS EC2 makes this process easier by providing virtual servers (called instances) that can be used to deploy our applications to Staging. Once our application is deployed to the EC2 instance, we can test it in the Staging environment to ensure that it works as expected. Using AWS EC2 to deploy our application to Staging helps us catch potential issues early and reduce the risk of introducing bugs or other issues into production. Additionally, AWS EC2 provides a reliable and scalable platform for deploying and testing applications."
            }
        }
        stage('Integration Tests on Staging'){
            steps{
                echo "Running Tests...."
            }
            post{
                success{
                    mail to: "arshsure@gmail.com",
                    subject: "Integration Tests on Staging Status Email",
                    body: "Integration Tests on Staging was a success"
                }
            }
        }
        stage('Deploy to Production'){
            steps{
                echo "Deploying..."
                echo "Automation for build after commit"
            }
        }
    }
}
