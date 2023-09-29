pipeline {
    agent any

    stages {
        stage('Git Clone') {
            steps {
                // Hier halen we de code op uit je GitHub-repository.
                // Vervang 'https://github.com/jouw-gebruikersnaam/jouw-repo.git' door de URL van je GitHub-repository.
                git branch: 'main', credentialsId: 'jouw-credentials-id', url: 'https://github.com/Sam233124/Sam1.git'
            }
        }

        stage('Copy HTML to Apache') {
            steps {
                // Hier kopiëren we de HTML-bestanden naar de Apache-webserver.
                // Vervang '/path/to/your/html/files' door het pad naar je HTML-bestanden op de Jenkins-agent.
                sh "cp -r /path/to/your/html/files/* /var/www/html/"
            }
        }
    }

    post {
        success {
            echo 'De HTML-code is succesvol gekopieerd naar de Apache-webserver.'
        }
    }
}
