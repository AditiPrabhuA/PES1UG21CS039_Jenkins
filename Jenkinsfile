pipeline{
  agent any
  stages{
    stage('Clone repository') {
    //   steps{
    //     cjeckout([$class: 'GitSCR',
    //               branches: [[name: '*/main']],
    //               userRemoteConfigs: [[url: 'https://github.com/AditiPrabhuA/PES1UG21CS039_Jenkins.git']]])
    //   }
    // }
    stage('Build') {
      steps{
        build 'PES1UG21CS039-1'
        sh 'cd main \n g++ test.cpp -o output'
      }
    }
    stage('Test') {
      steps{
        sh './output'
      }
    }
    stage('Deploy') {
      steps{
        echo 'deploy'
      }
    }
  }
  post{
    failure{
      error 'Pipeline failed'
    }
  }
}
