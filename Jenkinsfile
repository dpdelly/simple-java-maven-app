pipeline {
    agent any
    tools {
        maven 'maven-3-5-2'
        jdk 'jdk8'
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
		sh 'file 55'
            }
            post {
                always {
                    junit 'target/surefire-reports/*.xml'
                }
            }
        }
    }
}
