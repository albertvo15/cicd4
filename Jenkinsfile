pipeline {
    agent { docker { image 'python:3.5.1' } }
    stages {
        stage('build') {
            steps {
                sh 'python --version'
            }
        }
        stage('Test') {
            steps {
                sh 'date'
            }
        }
    }
}

//node {
//  echo "hello 2"
//  git url: 'https://github.com/jglick/simple-maven-project-with-tests.git'
//  def mvnHome = tool 'M3'
//  sh "${mvnHome}/bin/mvn -B verify"
//  sh "${mvnHome}/bin/mvn -B install"
//}
