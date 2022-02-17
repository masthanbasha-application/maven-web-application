node
{

def mavenHome = tool name: "maven3.8.4"
stage('CheckoutCode')
{
git branch: 'development', credentialsId: '997567eb-817e-4c2d-9719-a27955b7dab3', url: 'https://github.com/masthanbasha-application/maven-web-application.git'    
}

stage('Build')
{
 sh "${mavenHome}/bin/mvn clean package"
}
/*
stage('ExecuteSonarqube')
{
sh "${mavenHome}/bin/mvn sonar:sonar"
}
stage('UploadArtifactInNexus')
{
sh "${mavenHome}/bin/mvn deploy"
}

stage('DeployApplicationInTomcat')
{
sshagent(['4126dd0f-60e3-4bef-b078-d44a7eda2738']) 
{
sh "scp -o StrictHostKeyChecking=no target/maven-web-application.war ec2-user@3.109.181.94:/opt/apache-tomcat-9.0.58/webapps/"
}
}

stage ('SendEmailNotification')
{
mail bcc: '', body: '''Build over..

Regards,
MasthanBasha,
9704765605.''', cc: '', from: '', replyTo: '', subject: 'Build over', to: 'skmasthanbasha96@gmail.com'
}

stage('JobProperties')
{
properties([buildDiscarder(logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '5', daysToKeepStr: '', numToKeepStr: '5')), pipelineTriggers([pollSCM('''* * * * *
''')])])
}
 */
}
