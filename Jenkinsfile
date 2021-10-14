pipeline {
    agent any
    tools {
        // version de maven instalada y configurada con el nombre de "M3"
        maven "M3"
    }
    stages {
        stage("Maven Build"){
            steps {
                echo 'Build jar'
                sh "mvn clean install"
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