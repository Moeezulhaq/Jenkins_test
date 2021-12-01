pipeline {
 agent any
 stages {
  stage('Build') {
   steps {
    echo 'Building..'
   }
  }
  stage('Test') {
   steps {
    echo 'Testing..'
   }
  }
  stage('Deploy') {
   steps {
    echo 'Deploying....'
   }
  }
  stage('slack notification') {
   steps {
    slackSend channel: 'moeez_testing', message: "Please Find status of Job status- ${currentBuild.currentResult} Build Name-${env.JOB_NAME} Build Number-${env.BUILD_NUMBER} Build URL-${env.BUILD_URL}"
   }   
  }
 }
}

    
}