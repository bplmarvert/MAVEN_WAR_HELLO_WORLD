spipeline{
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
                sh "docker build . -t bmourrieras/MAVEN_WAR_HELLO_WORLD:${DOCKER_TAG} "
            }
        }     
    }
}
