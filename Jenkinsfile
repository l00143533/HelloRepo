pipeline {
agent any
// Get the Maven tool.
// NOTE: This Maven tool must be configured
// in the global configuration.
tools{
maven 'maven-3.6.3’
}
Stages{
stage(‘GIT Checkout’){
	steps{
		checkout([$class: ‘GitSCM’, branches: [[name: ‘*/master’]],
soGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: 
[], userRemoteConfigs: [[url: 'https://github.com/l00143533/HelloRepo’]]])
}
	}
stage('Build') {
		steps {
sh 'mvn -f JavaProject/pom.xml clean install'
		}
}
	
stage('Run Tests') {
steps {
sh 'mvn -f TestJavaProject/pom.xml test'
}
}
}
