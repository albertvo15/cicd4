pipeline {
    agent { any }
    stages {
        stage('git') {
            steps {
                sh "git clone https://github.com/jglick/simple-maven-project-with-tests.git"
                def mvnHome = tool 'M3'
            }
        }
        stage('Build') {
            steps {
                sh "${mvnHome}/bin/mvn -B install"
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
