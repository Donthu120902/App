  node{
   stage('SCM Checkout'){
     git  'https://github.com/javahometech/car-rentals.git'
   }
   stage('Compile-Package'){   
      sh 'mvn package '
   }
    stage('Deploy'){
      deploy adapters: [tomcat9(credentialsId: 'Deployment', path: '', url: 'http://65.0.131.44:8080/')], contextPath: '/pipeline-SPC', war: '**/*.war'
    }
}


