pipeline {
    agent any

    stages {
        stage('Trigger Builds') {
            steps {
                script {
                    // Define paths to Jenkinsfiles
                    def jenkinsfilePaths = [
                        '$pwd/dev/Jenkinsfile',
                        '$pwd/prod/Jenkinsfile',
                        // Add paths to other Jenkinsfiles as needed
                    ]
                    
                    // Trigger builds for each Jenkinsfile
                    for (def jenkinsfilePath : jenkinsfilePaths) {
                        build job: jenkinsfilePath, wait: false
                    }
                }
            }
        }
    }
}
