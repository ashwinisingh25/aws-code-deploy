pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                 withMaven(maven: 'localMaven'){
                    sh 'mvn clean compile'
                 }

            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                withMaven(maven: 'localMaven'){
                    sh 'mvn test'
                }
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
                withMaven(maven: 'localMaven'){
                    sh 'mvn deploy'
                }
            }
        }
    }
}