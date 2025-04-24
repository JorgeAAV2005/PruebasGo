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
                sh 'make tests'
            }
        }
    }

    post {
        always {
            junit 'test-report.xml' // Asegúrate de que el reporte se genere en este archivo
        }
    }
}
