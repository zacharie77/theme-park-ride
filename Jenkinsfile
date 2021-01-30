pipeline {
    agent any
    environment {
        PATH = "/opt/apache-maven-3.6.3/bin:$PATH"
    }
    stages {
        stage("clone code"){
            steps{
               git credentialsId: 'git_credentials', url: 'https://github.com/benjamaa-soufiene/theme-park-ride.git'
            }
        }
        stage("Build code"){
            steps{
              sh "mvn clean compile"
            }
        }
         stage("Test code"){
            steps{
              sh "mvn clean test"
            }
        }
         stage("Package code"){
            steps{
              sh "mvn clean package"
            }
        }
        stage("Install code"){
            steps{
              sh "mvn clean install"
            }
        
    }
}
