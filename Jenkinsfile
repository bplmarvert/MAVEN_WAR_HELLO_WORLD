spipeline{
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
            
        /*stage('Docker Build'){
            steps{
                sh "docker build . -t bmourrieras/MAVEN_WAR_HELLO_WORLD:0.1"
            }
        } */    
    }
}
