pipeline {
    
    agent any

    parameters {
        string(name: 'Version', defaultValue: '1.0.3' , description: 'Version Value')
    
    }
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
                sh 'echo "Deploying Version is ${params.Version}"'

            }
        }
        stage ('Clean'){
            steps {
                sh 'echo "Cleaning the Application... "'

            }
        }
    }
}
