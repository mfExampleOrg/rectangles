pipeline {
    agent any
    tools {
        maven 'MAVEN3' 
        jdk 'JDK9'
    }

    stages {
        stage('Build') {
            steps {
                script {
                    if(isUnix()) {
                        sh 'mvn clean install'
                    }
                    else {
                        bat 'mvn clean install'
                    }
                }
            }
        }
    }
}
