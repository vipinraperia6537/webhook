pipeline {
    agent any
    stages {
        stage('new') {
            steps {
                git 'https://github.com/opstree/spring3hibernate'
            }
        }
        stage("code stability") {
            steps{
                sh "mvn compile"
            }
        }
        stage("code quality"){
            steps{
                sh "mvn checkstyle:checkstyle"
            }
        }
        stage("code covering"){
            steps{
                sh "mvn cobertura:cobertura"
  
