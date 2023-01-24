pipeline {
    agent any
    stages {
        stage('Build App') {
            steps {
                sh 'docker build -t ngx .'
                sh 'docker container rm -f myngx || echo "no conta"'
                sh 'docker run --name myngx -dp 80:80 ngx'
            }
        }
    }
}
