node {
  stage('SCM') {
    checkout scm
  }
  stage('SonarQube Analysis') {
    def mvn = tool 'Default Maven';
    withSonarQubeEnv("ee89") {
      sh "${mvn}/bin/mvn clean install sonar:sonar"
    }
  }
}
