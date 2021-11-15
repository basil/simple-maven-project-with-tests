node {
  stage('Checkout') {
    sleep 5
    checkout scm
    sleep 5
  }
  stage('Build') {
    while (true) {
      sh 'mvn -B -ntp -Dmaven.test.failure.ignore clean verify'
      sleep 5
    }
  }
  stage('Collect results') {
    junit '**/target/surefire-reports/TEST-*.xml'
  }
}
