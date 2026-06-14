pipeline {
    agent any

    stages {

        stage('Build Image') {
            steps {
                sh 'docker build -t news-dashboard .'
            }
        }

        stage('Run Container') {
            steps {
                sh '''
                docker stop news-dashboard || true
                docker rm news-dashboard || true

                docker run -d \
                    --name news-dashboard \
                    -p 8080:80 \
                    news-dashboard
                '''
            }
        }
    }
}
