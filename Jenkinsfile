



pipeline{
  agent any
  stages{
    stage('System Check & Jenkins Status & Current User'){
      parallel{
        stage('System Statistics'){
          steps{
            sh 'lsblk'
            sh 'echo System check is complete' 

          }
        }
        stage('Status of Jenkins'){
          steps{
            sh 'sudo systemctl status jenkins'
            sh 'echo Jenkins is running'  
          }
        }
      }
    }
    stage('Linux User'){
    	steps{
    		sh 'whoami'
    		sh " echo The current user is Bukola"
    	}
    }
  }
}
