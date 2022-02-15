pipeline {
    agent any

    stages {
        stage('CD') {
            steps {
                git 'https://vinod_dega@bitbucket.org/uigw/rype_spa.git'
            }
        }
        stage('CB') {
            steps {
                sh 'npm install'
                sh 'npm run build'
            }
        }
        
    }
}
