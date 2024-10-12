pipeline {
  agent any
  stages {
    stage('Verify browsers are installed') {
      steps {
        powershell """
          Test-Path "C:\Program Files\Google\Chrome\Application\chrome.exe" 
        """
      }
    }
    stage('Run Tests') {
      steps {
        bat 'mvn clean test'
      }
    }
  }
}