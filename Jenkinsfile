pipeline {
    agent {
    label 'Agent-1'
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