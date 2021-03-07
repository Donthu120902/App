  node{
   stage('SCM Checkout'){
     git  'https://github.com/wakaleo/game-of-life.git'
   }
   stage('Compile-Package'){   
      sh 'mvn package '
   }
    stage('Deploy'){
      deploy adapters: [tomcat9(credentialsId: 'Deployment', path: '', url: 'http://65.0.131.44:8080/')], contextPath: '/pipelineJob', war: '**/*.war'
    }
}


