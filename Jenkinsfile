pipeline {
    agent any

    stages {
        stage('Example') {
            steps {
                withCredentials([usernamePassword(credentialsId: 'my-secret', usernameVariable: 'USERNAME', passwordVariable: 'PASSWORD')]) {
                    echo "username: ${USERNAME}"
                    echo "password: ${PASSWORD}"
                }
            }
        }
    }
}