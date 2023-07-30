pipeline{
    agent any
    tools {
        nodejs "node18"
    }
    stages{
        stage("A"){
            steps{
                echo "========executing A========"
                sh "node index.js"
                sh "yarn -v"
            }
            post{
                always{
                    echo "========always========"
                }
                success{
                    echo "========A executed successfully========"
                }
                failure{
                    echo "========A execution failed========"
                }
            }
        }
    }
    post{
        always{
            echo "========always========"
        }
        success{
            echo "========pipeline executed successfully ========"
        }
        failure{
            echo "========pipeline execution failed========"
        }
    }
}