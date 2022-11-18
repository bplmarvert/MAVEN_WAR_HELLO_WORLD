pipeline{
    agent any
    tools {
      maven 'maven'
    }
    stages{
        
        stage('Maven Build'){
            steps{
                sh "mvn clean package"
            }
        }        
            
        stage('Docker Build'){
            steps{
                sh "docker build . -t kammana/hariapp:${DOCKER_TAG} "
            }
        }     
    }
}
