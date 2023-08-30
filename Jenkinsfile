

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
}
