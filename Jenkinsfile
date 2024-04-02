pipeline {
    agent {
    node{
        label 'maven'
    }
    }
    stages {
        stage('clone code') {
            steps {
               git branch: 'main', credentialsId: 'github-id', url: 'https://github.com/satyavathijagdeesh/cicd.git'
            }
        }
    }
}
