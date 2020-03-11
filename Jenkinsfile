pipeline {
    agent any
    stages{
         stage ('To Uninstalled docker on DTL Agent'){
                    agent{
            node {
                label("DTL-LIN1")
            }
        }
            steps{
                sh 'sudo yum remove docker -y'
            }
        }
        stage ('To Ininstalled docker on PROD Agent'){
            agent{
                node {
                    label("PROD-LIN1")
                }
            }
            steps{
                sh 'sudo yum remove docker -y'
            }
        }
           
    }
    post{
        always{
            cleanWS()
        }
    }
}
