pipeline{
  agent any 
  stages {
    stage('Build') {
      steps {
        build 'PES1UG21CS039-1'
        sh 'cd main \ng++ test.cpp -o output'
      }
    }
    stage('Test') {
      steps {
        sh './main/output'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploy'
      }
    }
  }
    post {
      failure {
        error 'Pipeline failed'
      }
    }
}
