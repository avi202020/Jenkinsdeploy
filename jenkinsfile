pipeline {

  agent { label 'kubepod' }

  stages {

    stage('Checkout Source') {
      steps {
        git url:'https://github.com/tharanii/Jenkinsdeploy.git', branch:'master'
      }
    }

    stage('Deploy App') {
      steps {
        script {
          kubernetesDeploy(configs: "Jenkinsdeploy", kubeconfigId: "mykubeconfig")
        }
      }
    }

  }
}