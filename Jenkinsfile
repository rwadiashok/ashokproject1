pipeline {
    agent any

    stages {
        stage('Verify Branch') {
            steps {
                echo '$GIT_BRANCH_Ashoks'
                
                 }
      }
      stage('Docker Build') {
         steps {
            pwsh(script: 'docker images -a')
            pwsh(script: """
               cd ashokproject1/
               docker images -a
               docker build -t jenkins-pipeline .
               docker images -a
               cd ..
            """)
        
                
            }
        }    
    }
    
}
