pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                 git branch: 'main', url: 'https://github.com/Subash770/Demo-Jenkins'
            }
        }

        stage('Build') {
            steps {
                bat 'mvn clean package'
            }
        }

        stage('Test') {
            steps {
                bat 'mvn test'
            }
        }

        stage('Archive Reports') {
            steps {
                junit '**/target/surefire-reports/*.xml'
            }
        }
    }
}
