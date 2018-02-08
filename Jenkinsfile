 pipeline {
    agent { 
        docker 'maven:3-alpine'
    }
    tools {
        maven 'M3' 
    }
    stages {
       stage('Git upload') { 
          steps {
              git 'https://github.com/RomanDelim/maven.git'
          }
       }
       stage('Building') {
            steps {
              sh "mvn package"
           }
        }
    }
}
