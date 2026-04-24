pipeline {
    agent any

    stages {
        stage('Descargar Código') {
            steps {
                echo 'Clonando el repositorio...'
                git credentialsId: 'github-token', 
                    url: 'https://github.com/25ciberdaniel/proyecto-devsecops.git', 
                    branch: 'desarrollo'
            }
        }
        stage('Construir Imagen Docker') {
            steps {
                echo 'Construyendo la imagen...'
                sh 'docker build -t mi-app-segura:latest .'
            }
        }
    }
}
