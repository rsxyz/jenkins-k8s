# jenkins-k8s

### Install jenkins

docker run -u 0 --privileged -d --name jenkins -p 8080:8080 -p 50000:50000 -v /var/run/docker.sock:/var/run/docker.sock -v $(which docker):/usr/bin/docker -v jenkins_home:/var/jenkins_home --name jenkins jenkins/jenkins:lts

### install plugins

# Kubernetes CLI Plugin

# Kubernetes Credentials Plugin

# Kubernetes Client API Plugin

### create credential secret file and load ~/.kube/config file

KUBECONFIG is credential id
