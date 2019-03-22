  node{
   stage('SCM Checkout'){
     git 'https://github.com/javahometech/my-app'
   }
   stage('Compile-Package'){
    
      def mvnHome =  tool name: 'Maven', type: 'maven'   
      sh "${mvnHome}/bin/mvn package"
   }
   stage('Gmail-Notification'){
    
      emailext body: '''Hi Jagadeesh ,

      Build success 

      Thanks''', subject: 'Build Notify', to: 'jagadeeshrules@gmail.com'
   }
   
}


