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
        stage("what files are there"){
            steps{
                sh "docker run -d -p 80:80 --name webapp nginx1"
                sh "docker run -d --name flaskapp flask-app"
            }
        }
    }
}