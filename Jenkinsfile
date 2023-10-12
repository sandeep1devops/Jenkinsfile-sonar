node {
  stage('SCM') {
    checkout scm
  }
  stage('SonarQube Analysis') {
    def scannerHome = tool 'sonarserver';
    withSonarQubeEnv("${sonarserver}") {
      sh "${scannerHome}/bin/sonar-scanner"
    }
  }
}
