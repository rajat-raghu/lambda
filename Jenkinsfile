node {
  stage('SCM') {
    checkout scm
  }
  stage('SonarQube Analysis') {
    //def scannerHome = tool 'SonarScanner';
    def scannerHome = tool name: 'sonar-scanner';
    withSonarQubeEnv() {
      sh "${scannerHome}/bin/sonar-scanner"
    }
  }
}
