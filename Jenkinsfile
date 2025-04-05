pipeline {
    agent any

    environment {
        SONAR_SCANNER_HOME = 'C:\\sonar-scanner-5.0.1.3006-windows\\bin'
        SONAR_HOST_URL = 'http://localhost:9000'
        SONAR_PROJECT_KEY = 'Ilyas Mohamed'
        SONAR_LOGIN = 'sqa_e8842f28249b1fb92365f09aae3e53f960f698bf'
    }

    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main', url: 'https://github.com/ilyasmohamed85/Jenkins1.git'
            }
        }

        stage('SonarQube Analysis') {
            steps {
                withSonarQubeEnv('Mohamed') {
                   bat 'C:\\sonar-scanner-5.0.1.3006-windows\\bin\\sonar-scanner -Dsonar.projectKey=Ilyas Mohamed -Dsonar.sources=src -Dsonar.host.url=http://localhost:9000 -Dsonar.login=sqa_e8842f28249b1fb92365f09aae3e53f960f698bf'
                }
            }
        }
    }
}
