pipeline {
    agent any

    stages {
        stage('Retrieve Credentials') {
            steps {
                script {
                    // Retrieve the secret credential by ID
                    withCredentials([usernamePassword(credentialsId: '145b8b5f-6eb9-40ca-9d96-e878c2781854', passwordVariable: 'SECRET_PASSWORD', usernameVariable: 'SECRET_USERNAME')]) {
                        
                        // Echo the username and password
                        echo "Username: ${SECRET_USERNAME}"
                        echo "Password: ${SECRET_PASSWORD}"
                    }
                }
            }
        }
    }
}