pipeline {
    agent {
      node {
        label 'workstation'
      }
    }
    stages {
        stage('Stage1') {
            steps {
                echo 'Hello world!' 
            }
        }

        stage('Stage2') {
            steps {
                echo 'Lets move on' 
            }
        }
    }

    post { 
        always { 
            echo 'I will always say Hello again!'
        }
    }
}