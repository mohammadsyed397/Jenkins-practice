pipeline{
    agent {
        label 'agent-1'
    }
    environment{
        course= 'jenkins'
    }
    options{
        timeout(time: 30,  unit: 'MINUTES')
        disableConcurrentBuilds()
    }

    stages{
        stage (build){
            steps{
                script{
                sh """
                    echo "hello pipeline"
                    env
                """
                }
            }
        }
        stage(test){
            steps{
                echo "testing"
            }
        }
        stage(deploy){
            steps{
                echo "deploy"
            }
        }
    }
    post{
        always{
            echo 'i will always say hello!!!'
            deleteDir()
        }
        success{
            echo 'Hello Success'
        }
        failure{
            echo 'Hello failure'
        }
    }
}