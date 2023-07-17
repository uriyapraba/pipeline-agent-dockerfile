pipeline
{
    agent none
    stages
    {
        stage('SCM-checkout')
        {
            agent any
            steps
            {
            checkout scmGit(branches: [[name: 'origin/dev']],
            userRemoteConfigs: [[ url: 'https://github.com/uriyapraba/pipeline-agent-dockerfile.git' ]])
            }
        }
        stage('Build-Dockerfile')
        {
            agent
            {
                dockerfile true
            }
            steps
            {
                sh 'cat /etc/lsb-release'
            }
        }
    }
}