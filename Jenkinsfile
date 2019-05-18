pipeline {
    agent any

    stages {
        stage ('SCM Checkout') {
            git 'https://github.com/Mukesh889/jenkins-example.git'
        }
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'Test_maven') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'Test_maven') {
                    sh 'mvn test'
                }
            }
        }
    }
}
