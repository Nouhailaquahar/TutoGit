pipeline {
    agent any
    stages {
        stage("Clone Git Repository") {
            steps {
                git(
                    url: "https://github.com/Nouhailaquahar/TutoGit.git",
                    branch: "main",
                    changelog: true,
                    poll: true
                )
            }
        }
    }
    post {
        success {
            echo "Le clonage du dépôt Git s'est bien déroulé."
        }
    }
}
