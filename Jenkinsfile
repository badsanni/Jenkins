pipeline {
    agent {
      node {
        label 'workstation'
      }
    }

    environment { 
        SURL = "test.femilab.com"
    }

    stages {
        stage('Stage1') {
            environment { 
                SURL = "stage.femilab.com"
            }

            steps {
                sh 'Hello world!, check out URL = ${SURL} ' 
            }
        }

        stage('Stage2') {
            steps {
                sh 'Lets move on, check out URL = ${SURL}' 
            }
        }
    }

    post { 
        always { 
            echo 'I will always say Hello again!'
        }
    }
}