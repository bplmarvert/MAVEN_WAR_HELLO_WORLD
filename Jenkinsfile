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
    }
}
