pipeline {
    agent { docker { image 'php' } }
    environment {
        DISABLE_AUTH = 'true'
        DB_ENGINE    = 'sqlite'
    }
    post {
        always {
            echo 'One way or another, I have finished'
            mail    to: 'jpaca1991@gmail.com',
                    subject: "Failed Pipeline",
                    body: "Something is wrong!"
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