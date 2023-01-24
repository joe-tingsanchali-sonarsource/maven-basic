node {
  stage('SCM') {
    checkout scm
  }
  stage('SonarQube Analysis') {
    def mvn = tool 'Default Maven';
    withSonarQubeEnv('ee98') {
      sh "${mvn}/bin/mvn clean verify sonar:sonar -Dsonar.projectKey=joe-tingsanchali-sonarsource_maven-basic_AYXlpVb5oKyJNQDo1azT -Dsonar.projectName=maven-interact-jenkins"
    }
  }
}
