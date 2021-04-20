node {

def mavenHome=tool name:  "maven3.6.3"

stage ('checkout')
{

git branch: 'main', credentialsId: 'cbe8554a-fbe7-4196-89bb-

85deccbc8cd4', url: 'https://github.com/mvimal28/testproject.git'

}

stage ('Build')
{
bat "${mavenHome}/bin/mvn clean package"

}

stage('ExecuteSonarQubeReport')
{

bat "${mavenHome}/bin/mvn sonar:sonar"
}

stage('UploadArtifactintoNexus')
{

bat "${mavenHome}/bin/mvn deploy"

}

stage('sendEmailNotification')
{
emailtext body: '''Build is over...

Regards,
Dudekula Rahulbasha
subject: 'Build is over', to: 'text@gmail.com'
}
}




 
