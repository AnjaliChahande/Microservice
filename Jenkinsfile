pipeline {
    agent any

    stages {
        stage('deployy to kubernetes') {
            steps {
                withKubeCredentials(kubectlCredentials: [[caCertificate: '', clusterName: 'EKS-cluster', contextName: '', credentialsId: 'k8-token', namespace: 'webapps', serverUrl: 'https://C5B163FFF834808EA901AFA9F7EAE944.gr7.us-east-1.eks.amazonaws.com']]) {
                    sh 'kubectl apply -f deployment-service.yml'
                    sleep 60

               }
            }
        }
        stage('deployy to kubernetes') {
            steps {
                withKubeCredentials(kubectlCredentials: [[caCertificate: '', clusterName: 'EKS-cluster', contextName: '', credentialsId: 'k8-token', namespace: 'webapps', serverUrl: 'https://C5B163FFF834808EA901AFA9F7EAE944.gr7.us-east-1.eks.amazonaws.com']]) {
                    sh 'kubectl get all -n webapps'

               }
            }
        }
    }
}
