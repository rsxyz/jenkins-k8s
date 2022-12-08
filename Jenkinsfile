

pipeline {
  
  agent any

  stages {
    stage('Install kubectl'){
      steps{
       sh 'curl -LO https://storage.googleapis.com/kubernetes-release/release/$(curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt)/bin/linux/amd64/kubectl'
       sh 'chmod +x ./kubectl && mv kubectl /usr/local/sbin'
      }
    }
    stage('Deploy App') {
      steps {
        withKubeConfig(credentialsId: 'KUBECONFIG') {
          sh "kubectl get nodes"
          sh "kubectl get pods"
        }
      }
    }
  }
}



