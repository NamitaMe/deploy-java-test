def dockerRun ='docker run -p 8080:8080 -d --name java-test namiducker/java-test:2.0.0 .'
pipeline {
    
    agent any 
    environment{
        DOCKER_IMAGE = 'namiducker/java-test:2.0.0'
    }
    
    stages{
        stage ('pull image from dockerhub'){
            steps{
                echo 'Starting to deploy docker image..'
                sh ' docker pull $DOCKER_IMAGE'
                //sh 'docker pull namiducker/java-test:2.0.0'
            }
        }
        stage ('deploy to server'){
            steps {
                
                echo 'hello'
                chmod 777 deploy.sh
                sh './deploy.sh'
                
                 //sh 'scp deploy.sh ${REMOTE_USER}@${REMOTE_HOST}:~/'
                 //sh 'ssh ${REMOTE_USER}@${REMOTE_HOST} "chmod +x deploy.sh"'
                 //sh 'ssh ${REMOTE_USER}@${REMOTE_HOST} ./deploy.ssh'
                }
            }
        }
            
}
