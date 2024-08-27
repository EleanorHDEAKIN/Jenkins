pipeline {
    agent any
    stages{
        stage('Build'){
            steps{
                echo "fetch the source code from the directory path specified by the environment variable. "
                echo "use Maven to compile the code and generate any necessary artifacts"
            }
        }
        stage('Unit and Integration Tests'){
            steps{
                echo "unit tests using JUnit to ensure functionality"
                echo "integration tests using Selenium to ensure functionality between components"
            }
        }

        stage('Code Analysis'){
            steps{
                echo "use SonarQube to check code quality"
            }
        }

        stage('Security Scan'){
            steps{
                echo "perform a security scan using OWASP"
            }
        }

        stage('Deploy to Staging'){
            steps{
                echo "deploy to staging server"
            }
        }

        stage('Integration Tests on Staging'){
            steps{
                echo "run integration tests on staging using Selenium"
            }
        }

        stage('Deploy to Production'){
            steps{
                echo "deploy to production server" 
            }
            post{
                success{
                    mail to: "hooperperson321@gmail.com",
                        subject: "Deploy successful",
                        body: "Build was successfully deployed",
                        attachlog: true
                }
                failure{
                    mail to: "hooperperson321@gmail.com",
                        subject: "Deploy failed",
                        body: "Build failed to be deployed",
                        attachlog: true
                }
            }
        }
    }
}
