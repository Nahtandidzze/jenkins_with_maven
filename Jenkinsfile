 pipeline {
    agent { 
        docker 'maven:3-alpine'
    }
    tools {
        maven 'M3' 
    }
    stages {
       stage('Preparation') { 
          steps {
              git 'https://github.com/RomanDelim/maven.git'
          }
       }
       stage('Example') {
            steps {
              sh "mvn package"
           }
        }
    }
}
