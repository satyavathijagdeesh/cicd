pipeline {
    agent {
    node{
        label 'maven'
    }
    }
    environment {
        PATH = "/opt/apache-maven-3.9.4/bin:$PATH"
    }
    stages {
       stage('clone code') {
            steps {
               git branch: 'main', credentialsId: 'github-id', url: 'https://github.com/satyavathijagdeesh/cicd.git'
            }
        }
        
        stage("build") {
            steps {
               sh 'mvn clean deploy'
            }
        }
    }
}

