pipeline{
    agent any
    stages{
        stage("clean up"){
            steps{
                sh "bash clean.sh || true"
            }
        }
        stage("build the images"){
            steps{
                sh "docker build -t nodejs-project ."
            }
        }
        stage("create the containers"){
            steps{
                sh "docker run -d -p 80:5000 --name nodejs-project nodejs-project"
            }
        }
    }
}