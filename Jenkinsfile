node{
  def mvnHome = tool name: 'mvn', type: 'maven'
  def sonarscanner= tool name: 'sonarscanner', type: 'hudson.plugins.sonar.SonarRunnerInstallation'
  stage('scm checkout'){
    git 'https://github.com/manjudevops591/multical.git'
}
  stage('Compile-package'){
    sh "${mvnHome}/bin/mvn package"
}
  stage('SonarQube Analysis') {
    withSonarQubeEnv('sonar-9') { 
    sh "${sonarscanner}/bin/scanner sonar:sonar"
        }
    }
}
