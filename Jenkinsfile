pipeline {
    agent {
        node {
            label 'AGENT-1'
        }
    }
    environment{
        COURSE = "Jenkins"
    }
    stages {
        stage( 'Build') {
            steps {
                script{
                    sh """
                        echo "Building"
                        echo $COURSE
                    """
                }
                echo "Building"
            }
        }
        stage('Test') {
            steps {
                script{
                    sh """
                        echo "Testing"

                    """
                }
                echo "Testing"
            }

        }
        stage('Deploy'){
            steps {
                script{
                    sh """
                        echo "Deploying"

                    """

                }
                echo "Deploying"

            }
        }

    }
    post{
        always{
            echo 'I will always say Hello again!'
            cleanWs()
        }
        success{
            echo 'i will run if sucess'
        }
        failure{
            echo 'I will run if failure'
        }

    }
}