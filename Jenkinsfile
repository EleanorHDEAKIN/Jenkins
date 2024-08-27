pipeline {
    agent any
    environment{
        DIRECTORY_PATH = "./code"
        TESTING_ENVIRONMENT = "environmentForTesting"
        PRODUCTION_ENVIRONMENT = "Eleanor"
    }
    stages{
        stage('Build'){
            steps{
                echo "fetch the source code from the directory path specified by the environment variable. "
                echo "compile the code and generate any necessary artifacts"
            }
        }
        stage('Test'){
            steps{
                echo "unit tests"
                echo "integration tests"
            }
        }

        stage('Code Quality Check'){
            steps{
                echo "check the quality of the code"
            }
        }

        stage('Deploy'){
            steps{
                echo "deploy the application to a testing environment specified by the environment variable"
            }
        }

        stage('Approval'){
            steps{
                sleep(10)
            }
        }

        stage('Deploy to Production'){
            steps{
                echo "deployed to $PRODUCTION_ENVIRONMENT" 
            }
        }
    }
}
