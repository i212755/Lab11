pipeline {
    agent any

    parameters {
        booleanParam(name: 'flag', defaultValue: true, description: 'Set flag to true or false')
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                // Add your build commands here
            }
        }

        stage('Test') {
            when {
                expression {
                    return params.flag == false
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
                echo 'Deploying... And test stage should be skipped'
                // Add your deployment commands here
            }
        }
    }
}
