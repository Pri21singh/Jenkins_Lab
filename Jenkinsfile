pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Pri21singh/Jenkins_Lab.git'
            }
        }
        stage('Build') {
            steps {
                echo 'Here is my App..'
            }
        }
        stage('Test') {
            steps {
                echo 'Tests looks good!!'
            }
        }
       stage('Notify') {
    steps {
        emailext subject: "Jenkins Build: ${currentBuild.currentResult}",
                 body: "Build ${currentBuild.displayName} finished with status: ${currentBuild.currentResult}",
                 to: 'singpri21@gmail.com',
                 replyTo: 'priyasingh2103@gmail.com',
                 attachLog: true
    }
}

    }
}
