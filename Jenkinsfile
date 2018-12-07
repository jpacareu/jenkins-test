pipeline {
    agent { docker { image 'php' } }
    environment {
        DISABLE_AUTH = 'true'
        DB_ENGINE    = 'sqlite'
        BUILD_URL    = 'localhost'
    }
    stages {
        stage('build') {
            steps {
                sh 'php --version'
                sh 'echo "Hello World ${env.BUILD_URL}"'
            }
        }
    }
}