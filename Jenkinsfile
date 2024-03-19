pipeline {
    agent any

    stages {
        stage('Trigger Builds') {
            steps {
                script {
                    def workspaceDir = env.WORKSPACE
                    // Define paths to Jenkinsfiles
                    def jenkinsfilePaths = [
                        '${workspaceDir}/dev/Jenkinsfile',
                        '${workspaceDir}/prod/Jenkinsfile',
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
