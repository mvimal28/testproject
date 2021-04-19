pipeline{
    agent any
    
    environment{
        PATH = "/opt/maven3/bin:$PATH"
    }
    stages{
        stage("Git Checkout"){
            steps{
                git credentialsId: 'cbe8554a-fbe7-4196-89bb-85deccbc8cd4', url: 'https://github.com/mvimal28/testproject.git'
            }
        }
}
