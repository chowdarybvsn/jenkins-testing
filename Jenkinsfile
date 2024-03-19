pipeline {
    agent any

    stages {
        stage('Trigger Builds') {
            steps {
                script {
                    def cwd = pwd()
                    // Define paths to Jenkinsfiles
                    def jenkinsfilePaths = [
                        '${cwd}/dev/Jenkinsfile',
                        '${cwd}/prod/Jenkinsfile',
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
