pipeline {
    agent { docker { image 'php' } }
    environment {
        DISABLE_AUTH = 'true'
        DB_ENGINE    = 'sqlite'
        BUILD_URL    = 'localhost'
    }
    post {
        always {
            mail to: 'jpaca1991@gmail.com',
                    subject: "Failed Pipeline",
                    body: "Something is wrong with"
        }
    }
    stages {
        stage('build') {
            steps {
                sh 'php --version'
                sh 'echo "Hello World"'
            }
        }
    }
}