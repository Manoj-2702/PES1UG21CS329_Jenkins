pipeline{
  agent any

  stages{
    stage('Build'){
      steps{
        build 'PESUG21CS329-1'
        sh 'g++ main/hello.cpp -o output'
      }
    }
    stage('Test'){
      steps{
        sh './output'
        sh 'exit 1'
      }
    }
    stage('Deploy'){
      steps{
        echo 'Display'
      }
    }
  }
  post{
    failure{
      echo 'Pipeline Failed'
    }
  }
}
