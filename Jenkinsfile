pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Cette étape récupère le code source depuis le dépôt Git
                checkout scm
            }
        }

        stage('Build') {
            steps {
                // Exécutez les commandes de build ici
                sh 'mvn clean package'
            }
        }

        stage('Test') {
            steps {
                // Exécutez les tests unitaires
                sh 'mvn test'
            }
        }

        stage('Deploy') {
            steps {
                // Ajoutez les étapes de déploiement ici
                // Par exemple, déployez l'application sur un serveur
            }
        }
    }

    post {
        success {
            // Actions à effectuer en cas de succès du pipeline
            echo 'Le pipeline a réussi!'

            // Ajoutez d'autres actions ici si nécessaire
        }

        failure {
            // Actions à effectuer en cas d'échec du pipeline
            echo 'Le pipeline a échoué. Vérifiez les logs pour plus d\'informations.'

            // Ajoutez d'autres actions ici si nécessaire
        }
    }
}
