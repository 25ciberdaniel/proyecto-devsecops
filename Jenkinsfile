pipeline {
    agent any
    stages {
        stage('Descargar Código') {
            steps {
                echo 'Clonando el repositorio con credenciales...'
                git credentialsId: 'github-token', 
                    url: 'https://github.com/25ciberdaniel/proyecto-devsecops.git', 
                    branch: 'desarrollo'
            }
        }
        stage('Construir Imagen Docker (Build)') {
            steps {
                echo 'Construyendo el contenedor seguro...'
                sh 'docker build -t mi-app-segura:latest .'
            }
        }
    }
}
