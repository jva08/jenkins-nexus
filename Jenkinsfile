pipeline {
    agent any
    tools {
        maven 'maven'
    }

    stages {

        stage('Build Maven') {
            steps{
                 git branch: 'main', credentialsId: 'devopshint', url: 'https://github.com/jva08/jenkins-nexus'
                 sh "mvn -Dmaven.test.failure.ignore=true clean package"
                
            }
        }   
    
    }
}
