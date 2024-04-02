pipeline {
    agent any

    stages {
    		stage('pre cleanup') {
                steps {
                    sh 'docker compose down'
                }
            }
            stage('git scm update') {
                steps {
                    git url: 'https://github.com/manuma159159/fastapi-app-01.git', branch: 'main'
                }
            }
            stage('docker build & deploy') {
                steps {
    				sh '''
    				docker compose up --build -d
    				'''
    			}	
        }
    }
}
