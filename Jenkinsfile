pipeline {
    agent any 
    environment {
      mvnHome = "/usr/share/maven"
    }
    tools {
        maven 'Maven3'
    }
    stages {
        stage('git') {
            steps {
//                sh "git clone https://github.com/jglick/simple-maven-project-with-tests.git"
//                git url: 'https://github.com/jglick/simple-maven-project-with-tests.git'
                git url: 'https://github.com/w3c/epubcheck.git'
            }
        }
        stage('Build') {
            steps {
//                sh "/usr/share/maven/bin/mvn -f my-app/pom.xml clean install"
//                sh 'mvn -f my-app/pom.xml clean install'
//                sh 'mvn install'
                sh 'mvn clean install'
            }
        }
        stage('Build2') {
            steps {
                sh 'cd my-app'
                sh 'mvn clean install'
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
