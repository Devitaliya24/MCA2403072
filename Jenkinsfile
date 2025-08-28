pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the project...'
                echo 'mvn clean package'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                echo 'mvn test'
            }
        }

        stage('Deploy') {
            when {
                branch 'main'
            }
            steps {
                echo 'Deploying to test environment...'
                echo './deploy.sh' 
            }
        }
    }
}
