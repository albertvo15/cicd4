pipeline {
    agent any 
    environment {
      mvnHome = "/usr/share/maven"
    }
    tools {
//        maven 'mavenHome'
        maven 'Maven3'
        jdk 'JavaHome'
    }
    stages {
        stage('git') {
            steps {
                sh "git clone https://github.com/jglick/simple-maven-project-with-tests.git"
            }
        }
        stage('Build') {
            steps {
                sh "/usr/share/maven/bin/mvn -f my-app/pom.xml clean install"
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
