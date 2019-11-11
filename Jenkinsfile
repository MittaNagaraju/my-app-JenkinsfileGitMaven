node{
   stage('SCM Checkout'){
     git 'https://github.com/MittaNagaraju/my-app-JenkinsfileGitMaven'
   }
   stage('Compile-Package'){
      // Get maven home path
      def mvnHome =  tool name: 'Maven', type: 'maven' 
      sh "${mvnHome}/bin/mvn package"
   }
   stage('Email Notification'){
      mail bcc: '', body: '''Hi welcome to jenkins email alerts
      thanks
      Nagaraju''', cc: '', from: '', replyTo: '', subject: 'Jenkins_Job', to: 'nagasai.mitta@gmail.com'
   }
   stage('Slack Notification'){
    
      slackSend baseUrl: 'https://hooks.slack.com/services/', 
         channel: '#learning', 
         color: 'good', 
         message: 'Welcome to Jenkins, Slack!', 
         tokenCredentialId: 'slack-demo', 
         username: 'naga86.iphone@gmail.com'
   }
}
