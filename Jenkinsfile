pipeline {
    agent any
    tools {
        nodejs '18.17.0'
    }
    
    stages {
        stage("Clone Git Repository") {
            steps {
                git(
                    url: "https://github.com/Nouhailaquahar/TutoGit.git",
                    branch: "master",
                    changelog: true,
                    poll: true
                )
            }
        }
        
        stage("Build and Run Angular Project") {
            steps {
                // Installer les dépendances Node.js
              dir("TutoGit"){
                sh "npm install"
                
                // Construire le projet Angular
              }
              //sh "ng build"
                
                // Exécuter le projet 
             //   sh "ng serve"
            }
        }
    }
    //post {
      //  success {
        //    echo "Le clonage du dépôt Git et l'exécution du projet Angular se sont bien déroulés."
        //}
    //}
}
