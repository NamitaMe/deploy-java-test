def dockerRun ='docker run -p 8080:8080 -d --name java-test namiducker/java-test:2.0.0 .'
pipeline {
    
    agent any 
    env{
        DOCKER_IMAGE = namiducker/java-test:2.0.0
    }
    
    stages{
        stage ('pull image from dockerhub'){
            steps{
                echo 'Starting to deploy docker image..'
                sh ' docker pull $DOCKER_IMAGE'
                //sh 'docker pull namiducker/java-test:2.0.0'
            }
        }
        stage ('Run container on dev server'){
            steps {
                
                echo 'hello'
                
                //sshagent(['centosprivatekey']) {
                   
                    //sh "ssh -o StrictHostKeyChecking=no ec2-user@172.31.3.215 ${dockerRun}"
                }
            }
        }
            
}
