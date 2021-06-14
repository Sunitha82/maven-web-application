node
{
  def mavenHome = tool name: "maven3.6.3"
	properties([buildDiscarder(logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '4', daysToKeepStr: '', numToKeepStr: '5')), [$class: 'JobLocalConfiguration', changeReasonComment: ''], pipelineTriggers([pollSCM('* * * * *')])])
  stage('CheckoutCode')
  {
   git branch: 'development', credentialsId: 'fb85d1fc-4b6f-475e-b5f8-55c6b4356921', url: 'https://github.com/Sunitha82/maven-web-application.git'
   }
  stage('Build')
  {
  sh "${mavenHome}/bin/mvn clean package"
  }
 /* stage('ExecuteSonarQubeReport')
  {
  sh "${mavenHome}/bin/mvn sonar:sonar
  }
  stage('UploadArtifactIntoNexus')
  {
  sh "${mavenHome}/bin/mvn deploy"
  }
  stage('DeployAppIntoTomcat')
  {
  sshagent(['a2f29894-52ba-442d-a341-00a4b2b21493']) {
    // some block
	sh "scp -o StrictHostKeyChecking=no target/maven-web-application.war ec2-user@18.118.55.65:/opt/apache-tomcat-9.0.46/webapps/"
	}
  }
  stage('sendEmailNotification')
  {
  mail bcc: '', body: 'Build Over', cc: 'sunitha.lakshman@gmail.com', from: '', replyTo: '', subject: 'Build Over', to: 'sunitha.lakshman@gmail.com'
  }
  }*/
 }
  
