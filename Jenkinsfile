pipeline{
    agent any
    
    stages{
        stage('Build'){
            steps{
                sh 'docker build -t flask:latest --name flaskapp .'
            }
        }
        stage('Deploy'){
            steps{
                sh 'docker run -d -p 3000:3000 flaskapp'
            }
        }
    }
}
