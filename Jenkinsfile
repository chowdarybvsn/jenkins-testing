pipeline {
   agent any
   
   stages{
       stage("first"){
          steps{
            script{
                def jenkinsfilePath = env.SCRIPT_NAME
                echo "Jenkinsfile Path: ${jenkinsfilePath}"
            }
          }
       }
   }
}