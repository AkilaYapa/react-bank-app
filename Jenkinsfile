pipeline{
    agent any
    stages{
        stage('Clone repository'){
            steps{
                git 'https://github.com/AkilaYapa/react-bank-app.git'
            }
        }
        stage('Verify environment'){
            steps{
                sh 'node -v'
                sh 'npm -v'
            }
        }
        stage('Install dependencies'){
            steps{
                sh 'npm install'
            }
        }
        stage('Run tests'){
            steps{
                sh 'npm test'
            }
        }
        stage('Build application'){
            steps{
                sh 'npm run build'
            }
        }
    }
    post {
        success {
            echo 'Build Successful'
        }

        failure {
            echo 'Build Failed'
        }
    }
}