pipeline {
  agent any
  stages {
    stage('OWASP') {
      steps {
        echo 'Checking'
        sh 'docker run --rm -v $(pwd):/zap/wrk/:rw owasp/zap2docker-stable zap-baseline.py -t http://localhost:8080 -r zap_report.html'
      }
    }

  }
}
