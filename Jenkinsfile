pipeline {
    agent any

    stages {
        stage('Cloner le dépôt') {
            steps {
                // Cloner le dépôt Git
                git url: 'https://github.com/azizamakh/Dernier.git', branch: 'codes'
            }
        }

        stage('Construire l\'image Docker') {
            steps {
                // Construire une image Docker en forçant l'utilisation de Bash
                sh 'bash -c "docker build -t image-app ."'
            }
        }

        stage('Exécuter le conteneur') {
            steps {
                // Lancer le conteneur Docker en forçant l'utilisation de Bash
                sh 'bash -c "docker run --rm image-app"'
            }
        }
    }
}
