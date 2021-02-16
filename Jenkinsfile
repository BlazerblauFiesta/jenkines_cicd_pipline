CODE_CHANGES = getGitChanges()
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
            when {
                expression {
                    BRANCH_Name == 'dev' && CODE_CHANGE == true
                }
            }
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
    post{
        // Execute Some Logic After all Stages excetted
        always{
            // Always Exexuted in all conditions
                steps {
                sh 'echo "Some Checking Steps... "'

            }
        }
        success {
                            steps {
                sh 'echo "Build Success... "'

            }
        }
        failure{
                                        steps {
                sh 'echo "Build Failed... "'

            }
        }
    }
}
