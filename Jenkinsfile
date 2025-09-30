// Jenkinsfile
pipeline {
    agent any // Run on any available agent

    triggers {
        cron('H/2 * * * *')
    }

    stages {
       stage('1. Checkout Code') {
         steps {
        // The fix is to explicitly tell Git which branch to use
        git branch: 'main', url: 'https://github.com/Sujalkahahai/jenkins_test.git'
    }
}

        stage('2. Compile Java Code') {
            steps {
                script {
                    if (isUnix()) {
                        sh 'javac hello.java'
                    } else {
                        bat 'javac hello.java'
                    }
                }
                echo 'Java code compiled successfully!'
            }
        }
    }
}
