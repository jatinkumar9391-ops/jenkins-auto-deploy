pipeline {
    agent any
    stages {
        stage('Pull Code') {
            steps {
                echo 'GitHub se code aa gya...'
                checkout scm
            }
        }
        stage('Build') {
            steps {
                echo 'Build kar raha hu...'
                sh 'ls -la'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploy kar raha hu...'
                sh 'sudo cp index.html /var/www/html/index.html'
                sh 'sudo systemctl restart apache2 || sudo systemctl restart nginx || echo "deployed"'
            }
        }
    }
}
