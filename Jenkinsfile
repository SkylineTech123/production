pipeline {
    agent any

    stages {
        stage('Dev') {
            steps {
                cleanWs()
                echo 'Building in dev environment'
                sh 'touch dev.txt'
            }
        }
        stage('Staging') {
            steps {
                echo 'Building in staging environment'
                 sh 'touch stage.txt'
            }
        }
        stage('prod') {
            steps {
                echo 'Building in prod environment'
                 sh 'touch prod.txt'
            }
        }
    }
     post {
        always {
            cleanWs() // Clean up the workspace to save disk space
        }
        success {
            echo "Pipeline finished successfully!"
        }
    }
}
