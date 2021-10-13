pipeline {
    agent any
    stages {
        stage("Maven Build"){
            steps {
                echo 'Build jar'
            }
        }
        stage("Docker Build"){
            steps {
                echo 'Build project image'
            }
        }
        stage("Deploy"){
            steps {
                echo 'Deploy to K8s'
            }
        }
    }
}