pipeline{
    agent any
    tools {
      maven 'maven'
    }
    environment {
        DOCKER_TAG = getVersion()
    }
    
    stages{
        
        stage('Maven Build'){
            steps{
                sh "mvn clean package"
            }
        }        
            
        stage('Docker Build'){
            steps{
                sh "docker build . -t bmourrieras/prjdevobs:0.1"
            }
        }  
    }
}
