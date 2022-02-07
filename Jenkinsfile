pipeline {
    agent any

    stages {
        stage('CD') {
            steps {
                git 'https://github.com/vinod102/flipkart-1.git'
            }
        }
        stage('CB') {
            steps {
                sh 'mvn install'
            }
        }
        stage('cd') {
            steps {
              'sshpass -p "root" scp target/flipkart-1.0-SNAPSHOT.jar root@172.17.0.3:/home/vinod/Distros/apache-tomcat-8.5.75/webapps'
            }   sh
        }
        
    }
}
