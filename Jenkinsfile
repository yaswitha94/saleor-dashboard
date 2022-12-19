pipeline{
    agent any
    triggers {
        pollSCM('* * * * *')
    }
    stages{
        stage('vcs') {
            steps{
              git  branch: 'main' , url: 'https://github.com/yaswitha94/saleor-dashboard.git'
            } 
        }
        stage('docker image build') {
            steps{
                sh 'docker image build -t yaswitha/saleor-dashboard:DEV .'
            }
        }
        stage('docker image push') {
            steps{
                sh 'docker push yaswithaa/saleor-dashboard:DEV'
            }
        }

    }
}