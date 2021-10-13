pipeline {
    agent any
    stages {
        stage("Maven Build"){
            echo 'Build jar'
        }
        stage("Docker Build"){
            echo 'Build project image'
        }
        stage("Deploy"){
            echo 'Deploy to K8s'
        }
    }
}