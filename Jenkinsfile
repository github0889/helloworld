node {
   
   	stage 'Stage 1'
   		echo 'helloworld, shell scripts'
   	stage 'Checkout'
   		git url: 'https://github.com/github0889/helloworld.git'
   	stage 'Build'
   		sh './myBuild.sh'
   	stage 'Deploy'
   		sh './myDeployment.sh'
  
}
