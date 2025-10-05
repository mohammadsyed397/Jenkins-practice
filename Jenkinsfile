pipeline{
    agent {
        label 'agent-1'
    }
    environment{
        course= 'jenkins'
    }
    options{
        timeout(time:10; unit: 'MINUTES')
    }

    stages{
        stage (build){
            steps{
                scripts{
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