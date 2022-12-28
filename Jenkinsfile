pipeline {
    agent any
    stages {
        stage('git repo & clean') {
            steps {
               //bat "rmdir  /s /q shadi"
                bat "git clone https://github.com/Dewank7852/shadi.git"
                bat "mvn clean -f shadi"
            }
        }
        stage('install') {
            steps {
                bat "mvn install -f shadi"
            }
        }
        stage('test') {
            steps {
                bat "mvn test -f shadi"
            }
        }
        stage('package') {
            steps {
                bat "mvn package -f shadi"
            }
        }
    }
}
