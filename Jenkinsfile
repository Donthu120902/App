  node{
   stage('SCM Checkout'){
     git 'https://github.com/javahometech/my-app'
   }
   stage('Compile-Package'){
    
      def mvnHome =  tool name: 'Maven', type: 'maven'   
      sh "${mvnHome}/bin/mvn package"
   }
   stage('Gmail-Notification'){
    
      mail bcc: '', body: '''Hi Jagadeesh,

      welcome to jenkins! your build got success.

      Thanks ''', cc: '', from: '', replyTo: '', subject: 'Jenkins Build Notify', to: 'jagadeeshrules@gmail.com'
   }
   
}


