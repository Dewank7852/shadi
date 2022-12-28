pipeline {
    agent any
    stages {
        stage('git repo & clean') {
            steps {
                sh "rmdir  /s /q shadi"
                sh "git clone https://github.com/Dewank7852/shadi.git"
                //sh "mvn clean -f shadi"
            }
        }
        stage('install') {
            steps {
                sh "mvn install -f shadi"
            }
        }
        stage('test') {
            steps {
                sh "mvn test -f shadi"
            }
        }
        stage('package') {
            steps {
                sh "mvn package -f shadi"
            }
        }
    }
}
