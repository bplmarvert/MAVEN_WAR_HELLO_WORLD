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
                sh "docker build . -t bmourrieras/prjdevobst0.1"
            }
        } 
        stage('DockerHub Push'){
            steps{
                withCredentials([string(credentialsId: 'docker-hub', variable: 'dockerHubPwd')]) {
                    sh "docker login -u bmourrieras -p ${dockerHubPwd}"
                }
                
                sh "docker push bmourrieras/prjdevobst0.1"
            }
        }
    }
}
