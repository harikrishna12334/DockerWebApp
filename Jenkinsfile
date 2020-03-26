properties([[$class: 'JiraProjectProperty'], parameters([choice(choices: 'master\nrelease\nbugfix', description: 'select the branch to build', name: 'branch')])]) && 
properties([[$class: 'JiraProjectProperty'], parameters([choice(choices: 'QA1\nQA2\nDEV\nUAT\nPROD', description: 'choose any ENV', name: 'ENV'), string(defaultValue: 'WIN', description: 'choose any platform', name: 'Platform', trim: false)])])

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
    }
}
  
