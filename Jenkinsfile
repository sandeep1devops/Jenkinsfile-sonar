node {
  stage('SCM') {
    checkout scm
  }
  stage('SonarQube Analysis') {
    def scannerHome = tool 'SonarScanner';
    withSonarQubeEnv("${sonarserver}") {
      sh "${scannerHome}/bin/sonar-scanner"
    }
  }
}
