pipeline {
    agent any
    tools {
        // version de maven instalada y configurada con el nombre de "M3"
        maven "M3"
        // version de docker instalada y configurada con el nombre de "docker"
        dockerTool "docker"
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
                sh "docker build -t simple-app ."
            }
        }
        stage("Deploy"){
            steps {
                echo 'Deploy to K8s'
                sh 'curl -LO "https://storage.googleapis.com/kubernetes-release/release/$(curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt)/bin/linux/amd64/kubectl"'
                sh 'chmod u+x ./kubectl'
                sh './kubectl version --client'
                sh './kubectl get pods'
            }
        }
    }
}