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
                sh "docker build -t flask-app ./python"
                sh "docker build -t nginx1 ./nginx"
            }
        }
        stage("create the containers"){
            steps{
                sh "docker run -d --name flask-app flask-app"
                sh "docker run -d -p 80:80 --name webapp nginx1"
            }
        }
    }
}