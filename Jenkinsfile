#!groovy

//@Library('common-jenkins-library')
//import common.vj.jenkins.*

//################################### Define Jenkins Pipeline specific configurations ##################################

//new PipelineBootstrap().createCommonAzureJenkinsPipeline().triggerCommonAzureJenkinsPipeline()

node('cloud') {  
    stage('Load jenkins scripts') {
      checkout scm      
    }

	  echo "Executing Build and Test..."
    
    stage('Build and Test') {       
       sh "mvn -B clean install -Dbuild.number=${BUILD_NUMBER}"
    }
}
