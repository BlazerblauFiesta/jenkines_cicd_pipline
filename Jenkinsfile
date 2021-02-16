pipeline {
    
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'echo "Building the Application... "'
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
