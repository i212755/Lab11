    def flag = true
    
    
    def flag = true
    
pipeline {
    agent any
    environment {
        VERSION = "2.2.4"
    }

    stages {
        stage('Build') {
            steps {
                echo "Building... with version ${VERSION}"
                echo 'Building...'
                // Add your build commands here
            }
        }
    
            stage('Test') {
                when {
                    expression {
                        return flag == false
                    }
                }
                steps {
                    echo 'Testing...'
                    // Add your test commands here
                }
            }
    
            stage('Deploy') {
                steps {
                    echo 'Deploying...And test stage should be skipped'
                    
                    // Add your deployment commands here
                }
            }
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


    
            stage('Test') {
                when {
                    expression {
                        return flag == false
                    }
                }
                steps {
                    echo 'Testing...'
                    // Add your test commands here
                }
            }
    
            stage('Deploy') {
                steps {
                    echo 'Deploying...And test stage should be skipped'
                    
                    // Add your deployment commands here
                }
            }
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
