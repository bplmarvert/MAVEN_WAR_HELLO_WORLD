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
                sh "docker build . -t bmourrieras/prjdevobs:0.1"
            }
        } 
        stage('DockerHub Push'){
            steps{
                    sh "docker login -u ${username} -p ${password}"
                }
                
                sh "docker push bmourrieras/prjdevops:0.1 "
            }
        }
    }
}
