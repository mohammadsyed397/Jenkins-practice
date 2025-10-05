pipeline{
    agent {
        label 'agent-1'
    }

    stages{
        stage (build){
            steps{
                echo "building"
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
            deleteDIR()
        }
        success{
            echo 'Hello Success'
        }
        failure{
            echo 'Hello failure'
        }
    }
}