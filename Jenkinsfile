pipeline {
    agent any
    stages {
        stage("Clone Git Repository") {
            steps {
                script {
                    def cloneResult = git(
                        url: "https://github.com/ssbostan/neptune.git",
                        branch: "master",
                        changelog: true,
                        poll: true
                    )
                    if (cloneResult == 0) {
                        currentBuild.result = 'SUCCESS'
                        echo "Le clonage du dépôt Git s'est bien déroulé."
                    } else {
                        currentBuild.result = 'FAILURE'
                        echo "Le clonage du dépôt Git a échoué."
                    }
                }
            }
        }
    }
    post {
        always {
            echo "Fin du pipeline."
        }
    }
}
