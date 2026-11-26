pipeline {
    agent {
    label 'Agent-1'
    } 
    environment{
        USER = 'Naveen'
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                
                echo 'Deploying....'
                sh 'pwd'
                sh 'ls -lrth'
                

            }
        }
        stage('Example') {
            environment { 
                AN_ACCESS_KEY = credentials('ssh-auth') 
            }
            steps {
                sh 'printenv'
            }
        }

    }


    post { 
        always { 
            echo 'I will always say Hello again!'
        }
        success{
            echo 'I will run when job success'
        }
        failure{
            echo 'I will run when job failure'
        }
        fixed{
            echo 'I will run when job got fixed'
        }
    }
}