pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                // Add your build commands here
            }
        }
        
    post {
        always {
            echo 'This will always run, regardless of the build result'
            // Add any post-build actions that should always run here
        }
        success {
            echo 'This will run only if the build is successful'
            // Add any post-build actions specific to success here
        }
        failure {
            echo 'This will run only if the build fails'
            // Add any post-build actions specific to failure here
        }
    }

        stage('Test') {
            when {
                expression {
                    return true // Adjust the condition as needed
                }
            }
            steps {
                echo 'Testing...'
                // Add your test commands here
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying...'
                sh 'nvm install'
                // Add your deployment commands here
            }
        }
    }

    
}
