pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/Subash770/Demo-Jenkins'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }

        stage('Archive Reports') {
            steps {
                junit '**/target/surefire-reports/*.xml'
            }
        }
    }
}
