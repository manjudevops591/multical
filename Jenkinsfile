node{
    stage('SCM Checkout'){
      git 'https://github.com/vijayakumar1/multical.git'
    }
    stage('Compile-Package'){
      def mvnHome = tool name: 'maven', type: 'maven'
      sh "${mvnHome}/bin/mvn package"
    }
    stage('deploy-to- tomcat'){
    
    }   
}
