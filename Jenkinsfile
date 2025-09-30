// Jenkinsfile
pipeline {
    agent any // Run on any available agent

    triggers {
        cron('H/2 * * * *')
    }

    stages {
        stage('1. Checkout Code') {
            steps {
                git 'https://github.com/Sujalkahahai/jenkins_test.git'
            }
        }

        stage('2. Compile Java Code') {
            steps {
                script {
                    if (isUnix()) {
                        sh 'javac HelloWorld.java'
                    } else {
                        bat 'javac HelloWorld.java'
                    }
                }
                echo 'Java code compiled successfully!'
            }
        }
    }
}
