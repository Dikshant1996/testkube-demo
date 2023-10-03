

pipeline {
    agent any // Use any available agent (including the master node)
    
    stages {
 
        
        stage('Create test') {
            steps {
                script {
                    // Run a Docker container with a custom script
                    sh """
                    #!/bin/bash
                    docker version
                    
                    """
                }
            }
        }
 
    }
    
    post {
        success {
            echo 'Docker container started successfully.'
        }
        failure {
            echo 'Failed to start Docker container.'
        }
    }
}

