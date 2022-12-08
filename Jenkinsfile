

pipeline {
  agent {
    kubernetes {
      	cloud 'kubernetes'
      	defaultContainer 'jnlp'
      }
    }
  stages {
    stage('Deploy App') {
      steps {
        script {
          kubernetesDeploy(configs: "k8s-nginx-service-deploy.yaml", kubeconfigId: "MINIKUBE")
        }
      }
    }
  }
}



