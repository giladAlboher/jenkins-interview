pipeline {
    agent any
    environment {
        SECRET_FILE = credentials('jenkins-secret')
        MY_CREDENTIALS_USR = readFile("${SECRET_FILE}/username").trim()
        MY_CREDENTIALS_PSW = readFile("${SECRET_FILE}/password").trim()
    }
    stages {
        stage('Example') {
            steps {
                echo "Username: ${MY_CREDENTIALS_USR}"
                echo "Password: ${MY_CREDENTIALS_PSW}"
                // Use the credentials in your job steps
            }
        }
    }
}