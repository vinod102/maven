pipeline {
    agent any

    stages {
        stage('Get_Code_master') {
            steps {
                git 'https://github.com/AneesRavidKhan/DemoATC.git'
            }
        }
        stage('Build_Code') {
            steps {
                sh 'mvn install'
            }
        }
        stage('Deploy') {
            steps {
                sh 'scp target/DemoATR.war root@3.110.221.191:/var/lib/tomcat9/webapps'
            }
        }
    }
}
