pipeline {
    
    agent any
    
    environment {
        NEW_VERSION = '1.3.0'
    }
    
    stages {
        stage('Build') {
            steps {
                sh 'echo "Building the Application... "'
                sh 'echo "Building Version is ${NEW_VERSION}"'
                sh '''
                    echo "Multiline shell steps works too"
                    ls -lah
                '''
            }
        }
        stage ('Test'){
            steps {
                sh 'echo "Testing the Applications... "'
            }
        }
        stage ('Deply'){
            steps {
                sh 'echo "Deploying the Applications... "'

            }
        }
        stage ('Clean'){
            steps {
                sh 'echo "Cleaning the Application... "'

            }
        }
    }
}
