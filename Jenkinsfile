pipeline {

  stages { label 'kubepod' }
          

    stage('Checkout Source') {
      steps {
        git url:'https://github.com/rothmaan/CICD.git', branch:'master'
      }
    }

    stage('Deploy App') {
      steps {
        script {
          kubernetesDeploy(configs: "nginx.yaml", kubeconfigId: "mykubeconfig")
        }
      }
    }

  }

}
