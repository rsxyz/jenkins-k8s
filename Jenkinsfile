

pipeline {

  agent any

  stages {

    stage('Checkout Source') {
      steps {
        git url:'https://github.com/rsxyz/jenkins-k8s.git', branch:'main'
      }
    }

    stage('Deploy App') {
      steps {
        script {
          kubernetesDeploy(configs: "k8s-nginx-service-deploy.yaml", kubeconfigId: "MINIKUBE")
        }
      }
    }

  }

}