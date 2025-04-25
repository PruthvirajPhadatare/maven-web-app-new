pipeline {
    agent any
    stages {
        stage('Clone Repo') {
            steps {
                git changelog: false, poll: false, url: 'https://github.com/PruthvirajPhadatare/maven-web-app-new.git'
            }
        }
        stage('Code validation') {
            steps {
                sh 'mvn validate'
            }
        }
        stage('Clean Space') {
            steps {
                sh 'mvn clean'
            }
        }
        stage('Compile') {
            steps {
                sh 'mvn compile'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean install'
            }
        }
    }
}
