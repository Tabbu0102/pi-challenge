pipeline{
  agent any
  stages{
    stage('Clone repo') {
      steps{
        git 'https://github.com/Tabbu0102/pi-challenge.git/'
      }
    }
    stage('Calculate pi') {
      steps{
          script{
            def pi_value = sh(script: "python3 -c 'import math;
                              print(math.pi)'", returnStdout: true).trim()
                              echo "calculated value pf pi: ${pi_value}"
          }
      }
    }
  }
}
