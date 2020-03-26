currentBuild.displayName = "Reliance_Harikrishna_#"+currentBuild.number
pipeline{
	agent any
	
	options {
		buildDiscarder logRotator(daysToKeepStr: '5', numToKeepStr: '7')
	}
    stages{
      stage('SCM'){
        steps{
          git credentialsId: 'git_credentials', url: 'https://github.com/harikrishna12334/DockerWebApp.git' 
        }
      }
	stage('Maven Build - Clean'){
		steps{
			sh "mvn clean"
		}
	}
	stage('Maven Build - compile'){
		steps{
			sh "mvn compile"
		}
	}
	stage('Maven Build - Test'){
		steps{
			sh "mvn test"
		}
	}
	    
	    
	    
	    
	    
	    
	    
    }
}
  
