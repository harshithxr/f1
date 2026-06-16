pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git branch: 'master',
                url: 'https://github.com/USERNAME/MyMavenApp.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Run') {
            steps {
                sh 'java -jar target/MyMavenApp-1.0-SNAPSHOT.jar'
            }
        }
    }
}
