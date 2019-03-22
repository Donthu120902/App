  node{
   stage('SCM Checkout'){
     git 'https://github.com/javahometech/my-app'
   }
   stage('Compile-Package'){
    
      def mvnHome =  tool name: 'Maven', type: 'maven'   
      sh "${mvnHome}/bin/mvn package"
   }
    stage('Slack-Notification){
          slackSend baseUrl: 'https://hooks.slack.com/services/', channel: '#jenkinsnotifications', color: 'good', message: 'Build success ', teamDomain: 'Test-Domain', tokenCredentialId: 'Slackdemo'
          
          
          
   }
   
}


