properties([pipelineTriggers([githubPush()])])

node('linux') {   
	   
		url: 'https://github.com/JZangs/infrastructure-pipeline.git', branch: 'master'
	stage('Test') { 	
		sh 'env'   
	}
}
