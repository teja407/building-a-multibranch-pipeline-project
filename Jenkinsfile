pipeline {
    agent any
    stages {
	stage('init') {
            steps {
                sh 'echo "hello teja for development" '
            }
        }    
	
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
        stage('Test') {
        when {
                branch 'development' 
            }
	steps {
                sh './jenkins/scripts/deliver-for-development.sh'
            }
	}
    }
  
}
