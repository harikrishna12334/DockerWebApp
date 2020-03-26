pipeline {
  agent any 
    stages{
      stage('SCM'){
        steps{
          git credentialsId: 'git_credentials', url: 'https://github.com/harikrishna12334/DockerWebApp.git' 
        }
      }
    }
}
  
