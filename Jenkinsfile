pipeline {
    agent { label 'master' }
    stages {
        
        stage('Git pull code') {
            steps {
            git 'https://github.com/kudaykiran/jwtstarter.git'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }
         stage('deploy') {
            steps {
                sh 'java -jar -Dserver.port=1234 ./target/demo-0.1.0-SNAPSHOT.jar '    
                  }
          }
    }
}
