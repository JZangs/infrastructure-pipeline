properties([pipelineTriggers([githubPush()])])
node('linux') {
    git url: 'https://github.com/JZangs/infrastructure-pipeline.git', branch: 'master'
    stage('Test') {
        sh "env"
    }
    stage('GetInstances') {
         sh "aws ec2 describe-instances --region us-east-1"
    }

    stage ("CreateInstance") {
        sh "aws ec2 run-instances --image-id ami-467ca739 --count 1 --instance-type t2.micro --key-name SEISkey --security-group-ids sg-d5c6209c --subnet-id subnet-2bf1b714 --region us-east-1"

   }
}

