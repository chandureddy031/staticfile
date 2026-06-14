pipeline {
    agent any

    stages {

        stage('Deploy to EC2') {
            steps {
                sh '''
                sudo cp news_dashboard.html /var/www/html/index.html
                '''
            }
        }

    }
}