def flag = true

pipeline {
    agent any
    parameters {
        booleanParam(name: 'flag', defaultValue: true, description: 'Set flag to true or false')
        string(name: 'myVersion', defaultValue: '2.2.4', description: 'Specify the version')
    }
    stages {
        stage('Build') {
            steps {
                echo "Building... with version ${myVersion}"
                // Add your build commands here
                script {
                    echo "Building... with version ${params.myVersion}"
                    // Add your build commands here
                }
            }
        }
    }
}
