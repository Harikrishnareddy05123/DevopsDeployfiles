node
{
    properties([buildDiscarder(logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '', daysToKeepStr: '5', numToKeepStr: '')), pipelineTriggers([pollSCM('* * * * *')])]
    def mavenHome=tool name: "maven3.6.3"
    stage('Checkout')
    {
        git branch: 'development', url: 'https://github.com/Harikrishnareddy05123/maven-web-application.git'
        
    }
    stage('Build')
    {
    sh "${mavenHome}/bin/mvn clean package"     
    }
}
