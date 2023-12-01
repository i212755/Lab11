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
}
