pipeline {
    agent any

    stages {
        stage('Example') {
            steps {
                withCredentials([usernamePassword(credentialsId: '145b8b5f-6eb9-40ca-9d96-e878c2781854', usernameVariable: 'USERNAME', passwordVariable: 'PASSWORD')]) {
                    echo "username: ${USERNAME}"
                    echo "password: ${PASSWORD}"
                }
            }
        }
    }
}