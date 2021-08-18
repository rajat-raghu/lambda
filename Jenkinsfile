node {
  stage('SCM') {
    checkout scm
  }
  stage('SonarQube Analysis') {
    //def scannerHome = tool 'SonarScanner';
    def scannerHome = tool name: 'sonar-scanner', type: 'hudson.plugins.sonar.SonarRunnerInstallation';
    withSonarQubeEnv() {
      sh "${scannerHome}/bin/sonar-scanner"
    }
  }
}
