pipeline{
    agent {
        label "worker"
    }
    stages{
        stage("make a directory"){
            steps{
                sh "bash mkdir.sh || true"
            }
        }
        stage("where we at fam"){
            steps{
                sh "bash echo.sh"
            }
        }
        stage("what files are there"){
            steps{
                sh "bash file_location.sh"
            }
        }
        stage("add some files"){
            steps{
                sh "bash move.sh"
            }
        }
    }
}