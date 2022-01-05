def dockerRun ='docker run -p 8080:8080 -d --name java-test namiducker/java-test:2.0.0 .'
pipeline {
    
    agent any 
    
    stages{
        stage ('pull image from dockerhub'){
        }
        stage ('Run container on dev server'){
            steps {
                
                sshagent(['centosprivatekey']) {
                   
                    sh "ssh -o StrictHostKeyChecking=no ec2-user@172.31.3.215 ${dockerRun}"
                }
            }
        }
            
   }
    
}
