def flag = true
def VERSION = '1.0.0' // Replace with your actual version or define it as needed

pipeline {
    agent any
    parameters {
        booleanParam(name: 'flag', defaultValue: true, description: 'Set flag to true or false')
        booleanParam(name: 'ExecuteTests', defaultValue: true, description: 'Set flag to true or false')
        string(name: 'VERSION', defaultValue: '2.2.4', description: 'Specify the version')
    }

    stages {
        stage('Build') {
            steps {
                echo "Building... with version ${VERSION}"
                script {
                    echo "Building... with version ${params.VERSION}"
                    // Add your build commands here
                }
            }
        }
        stage('Test') {
            when {
                expression {
                    return !flag || !params.flag || params.ExecuteTests
                }
            }
            steps {
                echo 'Testing...'
                // Add your test commands here
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying... And test stage should be skipped'
                sh 'nvm install'
                // Add your deployment commands here
            }
        }
        // Add more stages as needed
    }

    post {
        always {
            echo 'This will always run, regardless of the build result'
            // Add any post-build actions that should always run here
        }
        failure {
            echo 'This will run only if the build fails'
            // Add any post-build actions specific to failure here
        }
    }
}
