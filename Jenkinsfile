pipeline {
    agent any

    stages {
        stage('Retrieve Credentials from YAML') {
            steps {
                script {
                    // Read the content of the jenkins-secret.yaml file
                    def secretYaml = readFile 'jenkins-secret.yaml'

                    // Parse the YAML content
                    def yamlData = readYaml text: secretYaml

                    // Retrieve username and password from the parsed YAML
                    def username = new String(Base64.getDecoder().decode(yamlData.data.username), 'UTF-8')
                    def password = new String(Base64.getDecoder().decode(yamlData.data.password), 'UTF-8')

                    // Echo the username and password
                    echo "Username: ${username}"
                    echo "Password: ${password}"
                }
            }
        }
    }
}
