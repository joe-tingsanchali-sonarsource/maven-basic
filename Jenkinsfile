node {
  stage('SCM') {
    checkout scm
  }
  stage('SonarQube Analysis') {
    def mvn = tool 'Default Maven';
    withSonarQubeEnv() {
      sh "${mvn}/bin/mvn clean verify sonar:sonar -Dsonar.projectKey=joe-tingsanchali-sonarsource_maven-basic_AYlLPYuk5zOrn6VeIc5L -Dsonar.projectName=maven-basic-jenkins-github -X"
    }
  }
}
