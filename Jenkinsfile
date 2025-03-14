pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Pri21singh/Jenkins_Lab'
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
                mail to: 'psingh0481@conestogac.on.ca',
                     subject: "Jenkins Build: ${currentBuild.currentResult}",
                     body: "Build ${currentBuild.displayName} finished with status: ${currentBuild.currentResult}"
            }
        }
    }
}
