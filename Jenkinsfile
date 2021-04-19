pipeline{
    agent any
    
    environment {
        PATH = "${PATH}:${tool name: 'Maven', type: 'maven'}/bin"
    }
    stages{
        stage("mvn Build"){
            steps{
                bat "mvn clean package"
            }
        }
    }
}




 