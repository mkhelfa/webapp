pipeline {
    agent {
        node {
            label 'slave-centos'        
        }
    }
    stages {
        stage('build1') {
            steps {
                sh 'svn --version'
            }
        }
        stage('build2') {
            agent { docker { image 'python:3.5.1' } }
            steps {
                sh 'python --version'
            }
        }
    }
}
