pipeline {
    agent { label 'agent3' }

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/JorgeAAV2005/PruebasGo.git'
            }
        }
        stage('Test') {
            steps {
                sh 'go test ./... -v -json > result.json'
            }
        }
    }

    post {
        always {
            // En Go los resultados no están en XML por defecto
            // Podés usar herramientas como go-junit-report si querés integración con JUnit
        }
    }
}
