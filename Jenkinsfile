pipeline{
    agent any
    stages{
        stage("make a directory"){
            steps{
                sh "mkdir ~/jenkins-pipelines || true"
            }
        }
        stage("where we at fam"){
            steps{
                sh "echo pwd"
            }
        }
        stage("what files are there"){
            steps{
                sh "ls -al"
            }
        }
        stage("add some files"){
            steps{
                sh "touch ~/jenkins-pipelines/file.txt"
                sh "mv ~/jenkins-pipelines/file.txt ~/jenkins-pipelines/file2.txt || true"
            }
        }
    }
}