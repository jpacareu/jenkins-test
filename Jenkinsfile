pipeline {
    agent { docker { image 'php' } }
    environment {
        DISABLE_AUTH = 'true'
        DB_ENGINE    = 'sqlite'
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