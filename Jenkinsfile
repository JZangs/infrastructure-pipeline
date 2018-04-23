properties([pipelineTriggers([githubPush()])])

node('linux') {   
	stage('Test') {    
		url: 'https://github.com/JZangs/infrastructure-pipeline.git'
		sh 'ant -buildfile test.xml'   
	}   
	stage('Build') {    
		sh 'ant'   
	}   
	stage('Results') {    
		junit 'reports/*.xml'   
	}
}
