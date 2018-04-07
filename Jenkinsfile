node {
  stage('SCM') {
    git 'https://github.com/anugpillai/sbtest.git'
  }
  stage('SonarQube analysis') {
    withSonarQubeEnv('SonarQube') {
      // requires SonarQube Scanner for Maven 3.2+
     sh 'mvn clean package sonar:sonar'
      
    }
  }
}
