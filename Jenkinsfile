pipeline {
    agent any
    stages{
        stage("Checkout code stage"){
            steps{
                git url:'https://github.com/prajwalreddy4/myrepo-jenkins.git', branch:'main'
            }
        }
        stage("Build docker image"){
            steps{
                sh 'docker build -t myimage .'
            }
        }
        stage("Create Container"){
            steps{
                sh 'docker run -d -p 8501:8501 --name="mycontainer" myimage'
            }
        }
    }

}