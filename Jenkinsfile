node {
   
   	stage 'Stage 1'
   		echo 'helloworld, shell scripts'
   	stage 'Checkout'
      //GitHub
   		git url: 'https://github.com/github0889/helloworld.git'
      stage ('Code Analysis') {
      //Sonarqube scanner with unit tests
    def scannerHome = tool 'SonarQube Scanner 7.4';
    withSonarQubeEnv('My SonarQube Server') {
      bat "${SONARQUBE_HOME}bin\windows-x86-64"
        }
      }	
      stage 'Build Automation'
      //Maven or Ant or Gradle
   		bat 'build.bat'
      stage 'Build Management'
      //Artifactory   
   	stage 'Deploy'
      //Tomcat or XL Deploy(less priority)
   		bat './myDeployment.bat'
      //Notify stage with email plugin configuration and required script.
}
