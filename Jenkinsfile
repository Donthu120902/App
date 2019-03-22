  node{
   stage('SCM Checkout'){
     git 'https://github.com/javahometech/my-app'
   }
   stage('Compile-Package'){
    
      def mvnHome =  tool name: 'Maven', type: 'maven'   
      sh "${mvnHome}/bin/mvn package"
   }
   stage('Email Notification'){
      mail bcc: '', body: '''Hi Welcome to jenkins email alerts, your build got succeded 
      Thanks
      DJ''', cc: '', from: '', replyTo: '', subject: 'Jenkins Job', to: 'jagadeeshdonthu15@gmail.com'
   }
   
}


