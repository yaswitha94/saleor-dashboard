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
                sh 'docker image build -t yaswithaa/saleor-dashboard1:DEV1 .'
            }
        }
        stage('docker image push') {
            steps{
                sh 'docker image push yaswithaa/saleor-dashboard1:DEV1'
            }
        }

    }
}
