node {
  stage('Checkout') {
    checkout scm
  }
  stage('Build') {
    sh 'mvn -B -ntp -Dmaven.test.failure.ignore verify'
  }
  stage('Collect results') {
    junit '**/target/surefire-reports/TEST-*.xml'
  }
}
