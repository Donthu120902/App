  node{
   stage('SCM Checkout'){
     git 'https://github.com/javahometech/my-app'
   }
   stage('Compile-Package'){
    
      def mvnHome =  tool name: 'Maven', type: 'maven'   
      sh "${mvnHome}/bin/mvn package"
   }
    stage('mail-Notification'){
    
      emailext body: '''Hi Jagadeesh,

      welcome to Jenkins , your build is success.

      Thanks''', subject: 'Build Notice ', to: 'jagadeeshrules@gmail.com'
    }
   
}


