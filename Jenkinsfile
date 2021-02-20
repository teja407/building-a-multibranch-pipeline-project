pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
        stage('Test') {
        when {
                branch 'production' 
            }
	steps {
                sh './jenkins/scripts/deploy-for-production.sh'
            }
	}
    }
  
}
