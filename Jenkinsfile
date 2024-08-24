pipeline {
    stages{
        stage("Checkout code stage"){
            step{
                git url:'https://github.com/prajwalreddy4/myrepo-jenkins.git',branch:'main'
            }
        }
        stage("Build docker image"){
            step{
                sh'docker build -t myimage .'
            }
        }
        stage("Create Container"){
            step{
                sh'docker run -d -p 8501:8501 --name="mycontainer" myimage'
            }
        }
    }

}