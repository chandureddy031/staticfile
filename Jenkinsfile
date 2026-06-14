pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git 'https://github.com/chandureddy031/staticfile.git'
            }
        }

        stage('Deploy to EC2') {
            steps {
                sh '''
                sudo cp news_dashboard.html /var/www/html/index.html
                '''
            }
        }
    }
}